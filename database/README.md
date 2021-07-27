# Database

## Table of Contents

인덱스

- 인덱스(index)란?
- 인덱스를 사용하면 검색 속도가 빨라지는 이유는? `보충`
- 인덱스 사용 시 UPDATE나 DELETE의 성능은 어떻게 될까?
- 인덱스의 장단점은?
- 인덱스를 생성하기에 적절한 컬럼의 특성은?
- 인덱스를 생성하기에 적절하지 않은 컬럼의 특성은?
- 인덱스를 생성하기 위한 SQL문 작성 방법은?
- 특정 테이블에 생성된 인덱스를 확인하기 위한 방법은?
- DML(INSERT, DELETE, UPDATE)을 수행할 때 인덱스를 사용하는 컬럼에 대해 추가로 해줘야 하는 작업은?
- 인덱스를 구현할 수 있는 자료구조에는 어떤 것들이 있을까?
- Hash Table로 구현하지 않는 이유는?
- = 연산과 <, >, between 연산의 예를 들어본다면?
- B+Tree란?
- B-tree란?
- B-tree가 성립하기 위한 조건들은?
- B-tree의 장점은?
- 범위 검색이 Hash table보다 B+ Tree에서 이점을 갖는 이유는?
- B-Tree보다 B+ Tree가 갖는 이점은?

트랜잭션

- 트랜잭션이란?
- 트랜잭션의 특징?
- 트랜잭션의 성질(ACID)?
- 트랜잭션의 연산?
- 트랜잭션의 상태?

정규화

- 정규화란?
- 데이터의 중복을 최소화함으로써 얻는 이득은?
- 제1 정규화에 대해 설명?
- 제2 정규화에 대해 설명?
- 제3 정규화에 대해 설명?
- BCNF에 대해 설명?

키

- 키란?
- 슈퍼키란?
- 후보키란?
- 기본키란?
- 대체키란?
- 외래키란?

SQL Query

- SQL이란?
- JOIN이란?
- INNER JOIN이란?
- OUTER JOIN이란?
- LEFT (OUTER) JOIN / RIGHT (OUTER) JOIN이란?
- CROSS JOIN(카티전 조인)이란?
- JOIN에서 ON과 WHERE의 차이점은?
- (OUTER) JOIN에서 (ON과 WHERE를 이용해서) 차집합을 구하는 방법은?

DBMS

- DBMS란?
- DBMS를 사용했을 때의 장점은?
- RDBMS란?

## 인덱스

### 인덱스(index)란?

추가적인 저장 공간을 활용해 테이블의 검색 속도를 향상시키기 위한 자료구조.

> - 인덱스를 저장하는 데 필요한 디스크 공간은 보통 테이블을 저장하는 데 필요한 디스크 공간보다 적다. 보통 인덱스는 키 - 필드만 가지고 있고, 테이블의 다른 세부 항목들은 가지고 있지 않기 때문이다.

---

### 인덱스를 사용하면 검색 속도가 빨라지는 이유는? `보충`

---

### 인덱스 사용 시 UPDATE나 DELETE의 성능은 어떻게 될까?

UPDATE와 DELETE의 성능도 함께 향상된다. UPDATE와 DELETE를 하기 위해서는 특정 대상을 조회해야 하기 때문이다.

ex) `UPDATE USER SET NAME = 'Lee' WHERE NAME = 'Shin';`

---

### 인덱스의 장단점은?

장점

- 테이블을 조회하는 속도를 향상시킬 수 있다.

단점

- 인덱스를 관리하기 위해 DB의 약 10%에 해당하는 저장 공간이 필요하다.
- 인덱스를 관리하기 위해 추가 작업으로 인한 오버헤드가 발생한다.

---

### 인덱스를 생성하기에 적절한 컬럼의 특성은?

- `WHERE`, `JOIN`, `ORDER BY`에 자주 사용되는 컬럼.
  (즉, 활용도가 높은 컬럼. 인덱스를 유지하는 오버헤드를 상회하는 활용도가 있어야 할 것이다.)
- `UPDATE`, `DELETE`가 자주 발생하지 않는 컬럼.
- 데이터의 중복도가 낮은 컬럼.
- 외래키로 사용되는 컬럼.

> - 또는, Cardinality(분산도)가 높은 컬럼. 즉 중복도가 낮은 컬럼.

---

### 인덱스를 생성하기에 적절하지 않은 컬럼의 특성은?

- `UPDATE`, `DELETE`가 빈번한 컬럼.

  이유: UPDATE와 DELETE 시 기존 인덱스 값을 삭제하지 않고 '사용하지 않음' 처리를 하기 때문에, 실제 데이터에 비해 인덱스의 크기가 과도하게 비대해질 수 있다.

- 데이터의 중복도가 높은 컬럼.

---

### 인덱스를 생성하기 위한 SQL문 작성 방법은?

```sql
CREATE INDEX [인덱스 명] ON [테이블 명]([컬럼 명]);
(ex) CREATE INDEX ind_email ON user(email);
```

---

### 특정 테이블에 생성된 인덱스를 확인하기 위한 방법은?

```sql
$ SHOW INDEX FROM [테이블 명];
```

> - 테이블 생성 시 PK를 설정해주면, 해당 컬럼이 자동으로 인덱스로 설정된다.

---

### DML(INSERT, DELETE, UPDATE)을 수행할 때 인덱스를 사용하는 컬럼에 대해 추가로 해줘야 하는 작업은?

- `INSERT`: 새로운 데이터에 대한 인덱스를 추가
- `UPDATE`: 기존 데이터의 인덱스를 사용하지 않도록 조치하고, 갱신한 데이터에 대한 인덱스를 추가
- `DELETE`: 삭제하는 데이터에 대한 인덱스를 더 이상 사용하지 않도록 조치

> DML(Data Manipulation Language): 데이터 삽입, 수정, 삭제

---

### 인덱스를 구현할 수 있는 자료구조에는 어떤 것들이 있을까?

- Hash Table
- B+Tree

---

### Hash Table로 구현하지 않는 이유는?

해시 테이블은 등호(`=`) 연산에만 최적화되어 있기 때문이다.

- 해시 테이블은 값이 1만 달라져도 완전히 다른 해시 값을 생성하는데,
- 부등호 연산(`<`, `>`)이나 `between` 등이 자주 사용되는 DB 검색에는 적합하지 않다.

---

### = 연산과 <, >, between 연산의 예를 들어본다면?

```sql
// =
SELECT * FROM member WHERE age = 27;
// <, >
SELECT * FROM member WHERE age < 30;
// BETWEEN
SELECT * FROM member WHERE age BETWEEN 20 and 30;
```

---

### B+Tree란?

- 확장된 버전의 B-tree.
- B-tree는 모든 노드에 key와 data를 담을 수 있다.
  B+tree는 브랜치 노드에는 key만 담아두고, 리프 노드에만 key와 data를 담을 수 있다.

> - B+tree의 리프 노드들은 Linked List로 연결되어 있다.
> - B+tree의 리프 노드들은 data로 실제 레코드를 찾아가기 위한 주소값을 가지고 있다.

---

### B-tree란?

- 확장된 버전의 이진 트리.
- 자식 노드의 개수가 2개 이상인 트리.

---

### B-tree가 성립하기 위한 조건들은?

- 노드의 데이터 수가 n개라면, 자식 노드의 개수는 n+1개여야 한다.
- 노드의 데이터는 정렬된 상태여야 한다.
- 노드의 데이터를 기준으로, 노드의 데이터보다 작은 값들은 왼쪽 자식 노드에, 큰 값들은 오른쪽 자식 노드에 위치해야 한다.
- 모든 리프 노드의 레벨은 같아야 한다. (→ "균형 트리")

---

### B-tree의 장점은?

- 빠른 탐색 속도: 평균 `O(logN)`
- 균일성: 어떤 값에 대해서도 같은 시간에 결과를 얻을 수 있다.

---

### 범위 검색이 Hash table보다 B+ Tree에서 이점을 갖는 이유는?

- B+tree의 리프 노드들은 Linked List로 연결되어 있기 때문에, 부등호, 범위 연산 등의 검색에 유리하다.

> - 물론 Hash Table의 검색 속도 `O(1)`에 비해 B+tree는 낮은 검색 속도 `O(logN)`을 가지고 있긴 하지만, 위의 장점으로 인해 B+tree를 사용한다.
> - 실제 InnoDB의 B+tree 구현에서는 Doubly Linked List로 구현이 되어 있다고 한다.

> (더 자세한 원리) Linked list라 부등호, 범위 연산 등의 검색에 유리하다?
>
> - 랜덤 I/O: 디스크 드라이브의 원판을 돌려 읽어야 할 데이터가 저장된 위치로 디스크 헤더를 이동시킨 후 읽는 것. (→ 디스크 헤더를 n번 움직인다.)
> - 순차 I/O: 랜덤 I/O와 같지만, 연속된 페이지에 접근하는 것이기에 한 번의 시스템 콜을 요청한다. (→ 디스크 헤더를 1번 움직인다.)
> - 디스크의 성능은 디스크 헤더의 위치 이동 없이 얼마나 많은 데이터를 읽고 쓰느냐에 따라 결정된다.

- B+tree에서 자식 노드로 이동하는 것, 혹은 Hash Table에서 이전 값과 1이라도 다른 값을 찾는 것은 모두 랜덤 I/O에 해당한다.
- B+tree에서 Linked List로 연결된 옆 자식 노드로 이동하는 것은 순차 I/O에 해당한다.

---

### B-Tree보다 B+ Tree가 갖는 이점은?

- 리프 노드를 제외하고는 key만 담고 있기 때문에, 더 많은 자료를 수용할 수 있다.
  (→ 더 많은 자식 노드 수용 → 더 낮은 트리 높이 → 더 높은 cache hit)

## 트랜잭션

### 트랜잭션이란?

데이터베이스의 상태를 변화시키기 위해 한번에 수행되어야 하는 일련의 연산들을 묶은 작업 단위

---

### 트랜잭션의 특징?

- 사용자가 데이터베이스 시스템에 대해 서비스를 요구할 때, 시스템이 응답하기 위한 상태 변환 과정의 작업 단위
- 하나의 트랜잭션은 commit되거나 rollback된다.

---

### 트랜잭션의 성질(ACID)?

Atomicity: 원자성

- 트랜잭션의 연산은 데이터베이스에 모두 반영되거나, 모두 반영되지 않아야 한다.

Consistency: 일관성

- 트랜잭션이 실행을 성공적으로 완료한 후에도 시스템의 고정요소는 언제나 일관성이 있어야 한다.

Isolation: 독립성

- 어느 하나의 트랜잭션이 다른 트랜잭션의 연산에 끼어들 수 없다.

Durability: 지속성

- 성공적으로 완료된 트랜잭션의 결과는 영구적으로 반영되어야 한다.

---

### 트랜잭션의 연산?

Commit

- 트랜잭션 작업이 성공적으로 끝났음을 알리는 연산

Rollback

- 트랜잭션이 비정상적으로 종료되었을 때의 연산
- 원자성을 위해 트랜잭션이 행한 모든 연산을 취소한다.

> - Rollback 시에는 해당 트랜잭션을 재시작하거나 폐기한다.

---

### 트랜잭션의 상태?

- 활동(Active): 트랜잭션이 실행 중인 상태
- 실패(Failed): 트랜잭션 실행에 오류가 발생해 중단된 상태
- 철회(Aborted): 트랜잭션이 비정상 종료되어 Rollback 연산을 수행한 상태
- 부분 완료(Partially Committed): 트랜잭션의 마지막 연산까지 실행했고, Commit 연산이 실행되기 직전의 상태
- 완료(Committed): 트랜잭션이 성공적으로 종료되어 Commit 연산을 실행한 후의 상태

## 정규화

### 정규화란?

테이블 간 데이터의 중복을 최소화하기 위해 데이터를 구조화하는 프로세스

---

### 데이터의 중복을 최소화함으로써 얻는 이득은?

무결성을 유지할 수 있다.

> 무결성(Integrity): 데이터의 정확성과 일관성을 유지하는 것

---

### 제1 정규화에 대해 설명?

테이블의 컬럼이 원자값을 갖도록 테이블을 구조화하는 것

![Database%2079d9527d1d534251afb6af40532b918b/Untitled.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled.png)

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%201.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%201.png)

---

### 제2 정규화에 대해 설명?

제 1정규화를 진행한 테이블에 대해,
완전 함수 종속을 만족하도록 테이블을 구조화하는 것

> 완전 함수 종속: 기본키의 부분 집합이 결정자가 되어서는 안된다는 것.

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%202.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%202.png)

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%203.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%203.png)

---

### 제3 정규화에 대해 설명?

제2 정규화를 진행한 테이블에 대해,
이행적 종속이 없도록 테이블을 구조화하는 것

> 이행적 종속: A→B, B→C일 때 A→C가 성립되는 것.

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%204.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%204.png)

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%205.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%205.png)

---

### BCNF에 대해 설명?

제3 정규화를 진행한 테이블에 대해,
모든 결정자가 후보키가 되도록 테이블을 구조화하는 것

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%206.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%206.png)

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%207.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%207.png)

## 키

### 키란?

무언가를 식별할 수 있는 고유한 식별자

---

### 슈퍼키란?

테이블에서 각 행을 유일하게 식별할 수 있는 하나 이상의 속성들의 집합

> - 즉, 유일성을 만족하면 슈퍼키이다.
>   (유일성: 하나의 키로 특정 행을 찾아낼 수 있는 고유한 속성)

---

### 후보키란?

테이블에서 각 행을 유일하게 식별할 수 있는 최소한의 속성들의 집합

> - 후보키는 기본키가 될 수 있는 후보들이다.
> - 유일성과 최소성을 동시에 만족해야 한다.

---

### 기본키란?

후보키들 중에서 하나를 선택한 키

---

### 대체키란?

후보키가 두개 이상일 경우, 기본키 이외의 나머지 후보키

---

### 외래키란?

테이블의 속성 중 다른 테이블의 행을 식별할 수 있는 키

## SQL Query

### SQL이란?

RDBMS를 조작할 때 사용하는 언어

(예시)

```sql
/* SELECT */
> SELECT id, password FROM users;

> SELECT * FROM users WHERE id=2 OR id=3; // 또는 AND
> SELECT * FROM users WHERE NOT(id=2);

> SELECT * FROM users WHERE nick LIKE '%hee%'; // 전방일치('%hee'), 후방일치('hee%')

/* INSERT */
> INSERT INTO users VALUES(2, 'hee', 'gml3413@@', '2021-07-02');
> INSERT INTO users (id, name, password, createdAt) VALUES(2, 'hee', 'gml3413@@', '2021-07-02');

/* UPDATE */
> UPDATE users SET name=NULL; // WHERE 절이 없으면 모든 행이 수정됨.
> UPDATE users SET name='lee', createdAt='2021-07-19' WHERE id=2;

/* DELETE */
> DELETE FROM users; // 모든 행 삭제
> DELETE FROM users WHERE id=2;
```

---

### JOIN이란?

![Database%2079d9527d1d534251afb6af40532b918b/Untitled%208.png](Database%2079d9527d1d534251afb6af40532b918b/Untitled%208.png)

두개 이상의 테이블을 연결해서 데이터를 검색하는 방법

> - 테이블을 연결하려면 Primary key나 Foreign key 등 적어도 하나의 컬럼은 서로 공유되고 있어야 한다.

---

### INNER JOIN이란?

집합으로 치면 교집합에 해당하는 연산으로,
기준 테이블과 조인한 테이블 둘 다 가지고 있는 값만 검색된다.

```sql
> SELECT girl_group.id, girl_group.name, song.title
  FROM girl_group
  JOIN song // SQL에서 INNER JOIN은 간략히 JOIN으로 사용할 수 있다.
  WHERE girl_group.hit_song_id = song.id;

// 만일 girl_group 중 hit_song_id가 NULL인 행이 있을 경우, 결과에 포함되지 않는다.
```

---

### OUTER JOIN이란?

조인하는 여러 테이블이 있을 때, 한쪽에는 데이터가 있고 한쪽에는 없을 때, 데이터가 있는 쪽 테이블의 내용을 모두 출력하는 것.

즉, 조건에 맞지 않아도 (한쪽 테이블의) 해당하는 행을 출력하는 것.

---

### LEFT (OUTER) JOIN / RIGHT (OUTER) JOIN이란?

왼쪽(혹은 오른쪽) 테이블의 행 중 조건절에 일치하지 않는 값을 가지고 있는 행도 가져온다.

```sql
> SELECT girl_group.id, girl_group.name, song.title
  FROM girl_group
  LEFT JOIN song
  WHERE girl_group.hit_song_id = song.id;

// girl_group 중 hit_song_id가 NULL인 행도 결과에 포함된다.
```

> - LEFT JOIN과 LEFT OUTER JOIN는 같은 용어이다.

---

### CROSS JOIN(카티전 조인)이란?

집합으로 치면 곱의 개념이다.

(A = { a, b, c, d }, B = { 1, 2, 3 } 일 때,
A CROSS JOIN B 는 (a,1), (a, 2), (a,3), (b,1), (b,2), (b,3), (c, 1), (c,2), (c,3), (d, 1), (d, 2), (d,3) 이다)

```sql
> SELECT girl_group.id, girl_group.name, song.title
  FROM girl_group
  CROSS JOIN song;

// 위 CROSS JOIN은 다음과 같이 나타낼 수도 있다.
> SELECT girl_group.id, girl_group.name, song.title
  FROM girl_group, song;
```

---

### JOIN에서 ON과 WHERE의 차이점은?

JOIN하는 범위가 다르다.

```sql
// 1번 쿼리
> SELECT *
  FROM A LEFT JOIN B
	ON (A.id = B.id)
	WHERE B.foo = 3;

// 2번 쿼리
> SELECT *
	FROM A LEFT JOIN B
	ON (A.id = B.id AND B.foo = 3);
```

1번 쿼리는

- A와 B 테이블을 LEFT JOIN한 후, WHERE절 조건에 해당하는 행만 추출한다.
- 즉, 결과값에는 `B.foo = 3`인 데이터만 존재한다.

2번 쿼리는

- ON 절로 LEFT JOIN한 행이 추출된다.
- 즉, 결과값에는 `B.foo = 3`이 아닌 데이터도 존재한다.

> - JOIN에서의 ON과 WHERE의 차이점을 이용해서 차집합을 구할 수 있다.

---

### (OUTER) JOIN에서 (ON과 WHERE를 이용해서) 차집합을 구하는 방법은?

```sql
> SELECT *
	FROM A LEFT JOIN B
	ON (A.id = B.id)
	WHERE B.id IS NULL;
```

## DBMS

### DBMS란?

사용자와 데이터베이스 사이에서,

- 사용자의 요구에 따라 정보를 생성해주고
- 데이터베이스를 관리해주는

소프트웨어

---

### DBMS를 사용했을 때의 장점은?

- 저장된 데이터를 여러 애플리케이션에서 공동으로 이용할 수 있다.
- 보안을 유지할 수 있다.

---

### RDBMS란?

행과 열을 가지는 표 형식의 2차원 데이터를 저장하는 DB
