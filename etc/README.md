# Etc

## Table of Contents

객체 지향 프로그래밍(OOP)

- 객체 지향 프로그래밍이란?
- 객체 지향 프로그래밍의 장단점은?
- 절차 지향 프로그래밍이란?
- 클래스와 인스턴스(객체)란?
- 오버로딩(Overloading)과 오버라이딩(Overriding)의 차이점은?
- 객체 지향 5대 원칙에 대해 설명해본다면?

## 객체 지향 프로그래밍(OOP)

### 객체 지향 프로그래밍이란?

프로그램을 (명령어의 목록으로 보는 시각에서 벗어나) 여러 개의 독립된 단위인 객체의 모임으로 파악하고자 하는 것. 각각의 객체는 메시지를 주고받고, 데이터를 처리할 수 있다.

특징

1. 추상화

   - 객체들의 공통적인 특징을 도출하는 것.
     > - 객체 지향 프로그래밍에서 추상화는 클래스를 정의하는 것을 말한다. 즉, 공통의 속성이나 기능을 묶고 이름을 붙여 변수와 메서드로 정의하는 것이다.

1. 캡슐화

   - 데이터와 기능을 묶어 외부에 드러나지 않도록 정보를 은닉하는 것.
     > 캡슐화의 목적
     >
     > - 코드의 재활용: 관련된 특성과 기능이 한 곳에 모여 객체의 재활용이 원활해진다.
     > - 정보 은닉: 외부에 노출되어서는 안되는 정보를 접근 제어자를 통해 은닉함으로써 책임이 있는 객체만 수정할 수 있고, 예측이 원활해진다.

1. 상속

   - 하나의 클래스가 가진 데이터와 함수를 다른 클래스가 그대로 물려받는 것.

1. 다형성

   - 동일한 이름의 함수가, 연결된 객체에 따라 다르게 해석되는 것.
   - 오버라이딩(Overriding)과 오버로딩(Overloading)이 다형성을 보장한다.

---

### 객체 지향 프로그래밍의 장단점은?

장점

- 생산성: 상속, 다형성 등을 통해 코드를 재사용하기 쉽다. (이미 만들어진 클래스를 상속받거나, 객체를 가져다 재사용하거나, 부분만 수정함으로써 소프트웨어 작성 부담을 대폭 줄일 수 있다.)

- 모델링 용이: 실세계를 모델링할 때, 하나의 절차로 모델링하는 것보다 객체 간 상호작용으로 모델링하는 것이 훨씬 쉽다.

- 보안성: 캡슐화를 통해 구현되는 부분이 외부에 드러나지 않도록 은닉할 수 있다.

단점

- 느린 실행 속도와 추가 메모리 공간: 캡슐화와 격리 구조로 인해 추가적인 포인터 크기와 메모리 연산 비용으로 인해 속도가 느리다.

---

### 절차 지향 프로그래밍이란?

어떤 기능을 어떤 순서로 처리하는가에 초점을 맞춰 개체를 순차적으로 처리하는 것.

장점

- 실행 속도가 빠르다: 컴퓨터의 처리 구조와 비슷하며, 추가적인 메모리가 필요하지 않아 연산이 빠르다.

단점

- 유지보수가 어렵다: 모든 구성 요소가 유기적으로 연결되어 있기 때문에, 하나가 고장났을 때 시스템 전체가 고장난다. 또한, 문제를 해결하기 위해 일부분이 아닌 시스템 전체를 수리해야 한다.

> 객체 지향과 절차 지향, 각각 어느 상황에서 사용하는 것이 좋을까?
>
> - 대형 프로그램의 경우, 많은 기능을 가지고 있기 때문에 객체 지향이 유리하다. 많은 역할을 객체로 묶을 수 있고, 재사용이 용이하기 때문이다.
> - 소형 프로그램의 경우, 절차 지향이 유리하다. 작은 기능을 객체로 나눌 경우 오히려 복잡해질 수 있기 때문이다.

---

### 클래스와 인스턴스(객체)란?

클래스

- 집단의 속성과 행위를 추상화를 거쳐 변수와 메서드로 정의한 것.
- 객체를 만들기 위한 메타 정보

인스턴스(객체)

- 클래스에서 정의한 것을 토대로 실제 메모리에 할당된 것.

---

### 오버로딩(Overloading)과 오버라이딩(Overriding)의 차이점은?

오버로딩: 같은 이름의 메서드를 여러 개 정의하고, 매개변수의 타입과 개수를 다르게 해 다양한 유형의 호출에 응답할 수 있도록 하는 것.

오버라이딩: 메서드의 이름, 매개변수, 반환형이 모두 같은 경우 상속받은 메서드를 덮어쓰는 것.

---

### 객체 지향 5대 원칙에 대해 설명해본다면?

1. 단일 책임 원칙(SRP, Single Responsibility Principle)

   - 클래스는 단 한 개의 책임을 가져야 한다.
     > 단 한 개의 '기능'을 가져야 한다는 의미로 해석할 수 있다. 이 원칙을 따르면 응집도는 높고, 결합도는 낮은 프로그램을 설계할 수 있다. 책임이 많아지면 클래스 내부 함수끼리의 결합도가 높아질 가능성이 많아진다. 이는 유지보수 비용을 높인다.
     >
     > - 결합도(coupling): 어떤 기능이 다른 클래스나 모듈에 얼마나 의존적인지를 나타낸다.
     > - 응집도: 객체 안의 모듈 간 요소가 얼마나 밀접한 관련이 있는 것들로 구성되어 있는지를 나타낸다.

2. 개방-폐쇄 원칙(OCP, Open-Closed Principle)

   - 확장에는 열려 있어야 하고, 변경에는 닫혀 있어야 한다.

     > 기존의 코드를 변경하지 않고(Closed) 기능을 수정하거나 추가할 수 있어야 한다(Open)는 말이다. 이 원칙을 따르면 변경에 유연하므로 유지보수 비용을 줄여주며, 코드의 가독성이 좋아진다.

     ```java
     // OCP를 위배하는 코드
     class SoundPlayer {
         void play() {
             System.out.println("play Wav"); // wav 재생
         }
     }

     public class Client {
         public static void main(String[] args) {
             SoundPlayer sp = new SoundPlayer();
             sp.play();
         }
     }
     // - SoundPlayer가 wav 이외의 다른 포맷을 재생할 수 있도록 요구사항이 변경되면 SoundPlayer의 play() 메소드를 수정해야만 한다.

     // OCP를 만족시키는 코드
     // 여러가지 방법이 있지만, 그 중 interface를 활용하는 예시이다.
     interface playAlgorithm {
         public void play();
     }
     // play()를 interface로 분리한다.

     class Wav implements playAlgorithm {
         @Override
         public void play() {
             System.out.println("Play Wav");
         }
     }

     class Mp3 implements playAlgorithm {
         @Override
         public void play() {
             System.out.println("Play Mp3");
         }
     }

     class SoundPlayer {
         private playAlgorithm file;

         public void setFile(playAlgorithm file) {
             this.file = file;
         }

         public void play() {
             file.play();
         }
     }

     public class Client {
         public static void main(String[] args) {
             SoundPlayer sp = new SoundPlayer();
             // (둘 중 원하는 파일 선택)
             sp.setFile(new Wav());
             sp.setFile(new Mp3());
             sp.play();
         }
     }
     // - 이와 같은 설계를 Strategy Pattern(전략 패턴)이라고 한다.
     // - SoundPlayer 클래스의 변경 없이 재생되는 파일을 변경할 수 있다.

     ```

3. 리스코프 치환 법칙(LSP, Liskov Substitution Principle)

   - 부모 클래스의 인스턴스 대신 자식 클래스의 인스턴스를 사용해도 문제가 없어야 한다.
   - 자식 클래스는 부모 클래스에서 가능한 행위를 수행할 수 있어야 한다.

     > 리스코프 치환 법칙은 일반화 관계에 대한 원칙이다. 상속 관계에서는 일반화 관계(IS-A)가 성립해야 한다.

     ```text
        예시) 도형 클래스와 사각형 클래스, 원 클래스가 있다. 사각형 클래스는 도형 클래스의 상속을 받는다.

        (1) 도형은 둘레를 가지고 있다.
        (2) 도형은 넓이를 가지고 있다.
        (3) 도형은 각을 가지고 있다.

        위 문장의 '도형' 단어를 '사각형'으로 바꾸면 이상한 부분이 없지만, '원'으로 바꾸면 (3)번 문장이 어색해진다. 이때 도형 클래스는 LSP를 만족하지 않는 설계라고 할 수 있다.

     ```

4. 인터페이스 분리 원칙(ISP, Interface Segregation Principle)

   - 한 클래스는 자신이 사용하지 않는 인터페이스를 구현하지 말아야 한다.
     > 즉 자신이 사용하지 않는 기능(인터페이스)에 영향을 받지 않아야 한다. 예를 들어 스마트폰으로 전화, 웹 서핑, 카메라 등의 기능을 사용할 수 있는데, 그 중 특정 기능을 사용할 때는 다른 기능을 사용하지 않을 것이다. 따라서 각각의 기능을 독립된 인터페이스로 구현해 서로에게 영향을 주고받지 않도록 설계해야 한다. 이 원칙은 시스템 내부 의존성을 약화시켜 리팩토링을 용이하게 한다.

5. 의존 역전 원칙(DIP, Dependency Inversion Principle)

   - 의존 관계를 맺을 때, 변화하기 쉬운 것보다 변화하기 어려운 것에 의존해야 한다는 원칙이다.
     > 변화하기 쉬운 것이란 구체적인 것을 말하고, 변화하기 어려운 것이란 추상적인 것을 말한다. 객체 지향의 관점에서 변화하기 쉬운 것은 구체화된 클래스를 말하고, 변화하기 어려운 것이란 추상 클래스나 인터페이스를 말한다. 따라서 DIP를 만족하기 위해서는 의존 관계를 맺을 때 구체화된 클래스보다는 인터페이스나 추상 클래스와 관계를 맺어야 한다.