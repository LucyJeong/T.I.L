# CS 기초
- **Static의 의미**
  - 클래스가 로딩될 때, 메모리 공간을 할당하는데 처음 설정된 메모리 공간이 변하지 않음을 의미
  - 객체를 아무리 많이 만들어도 해당 변수는 하나만 존재
- **OOP**
  - Object-Oriented Programming의 약어로써 객체지향 프로그래밍을 의미
  - 데이터를 객체로 취급하여 프로그램에 반영한 것이며, 순차적으로 프로그램이 동작하는 기존의 것들과는 다르게 객체와 객체의 상호작용을 통해 프로그램이 동작하는 것을 말한다.
  - OOP 특징
    - 코드 재사용성
    - 코드 변경 용이
    - 상속을 통한 장점 극대화
- **Overloading vs Overriding**
  - Overloading(오버로딩)
    - 같은 이름의 메소드를 여러개 정의하는 것
    - 매개변수의 타입이 다르거나 개수가 달라야 한다.
    - return type과 접근 제어자는 영향을 주지 않음.
  - Overriding(오버라이딩)
    - 상위 클래스(부모 클래스)의 메소드를 하위 클래스(자식 클래스)에서 재정의
      - ```i.e. overriding func viewDidLoad( ){ }```
- **Get /  Post**
  - Get 방식
    - 클라이언트에서 서버로 데이터를 전달할 때, 주소 뒤에 "이름"과 "값"이 결합된 스트링 형태로 전달
    - 주소창에 쿼리 스트링이 그대로 보여지기 때문에 보안성이 떨어짐
    - 길이 제한 있음(=전송 데이터의 한계가 있다.)
    - Post방식보다 상대적으로 전송 속도 빠름
  - Post 방식
    - 일정 크기 이상의 데이터를 보내야 할 때 사용
    - 서버로 보내기 전에 인코딩하고, 전송 후 서버에서는 다시 디코딩 작업
    - 주소창에 전송하는 데이터의 정보가 노출되지 않아 Get방식에 비해 보안성 높음
    - 속도가 Get방식보다 느림
    - 쿼리스트링(문자열) 데이터 뿐만 아니라, 라디오 버튼, 텍스트 박스 같은 객체들의 값도 전송가능
  - Get과 Post 차이점
    - Get은 주로 웹 브라우저가 웹 서버에 데이터를 요청할 때 사용
    - Post는 웹 브라우저가 웹 서버에 데이터를 전달하기 위해 사용
    - http://url/bbslist.html?id=5&pagenum=2 같이 하는 것이 GET방식이고 form을 이용해서 submit을 하는 형태가 POST
    - Get을 사용하면 웹 브라우저에서 웹 서버로 전달되는 데이터가 인코딩되어 URL에 붙음
    - Post방식은 전달되는 데이터가 보이지 않음
    - Get방식은 전달되는 데이터가 255개의 문자를 초과하면 문제가 발생할 수 있음  
    - 웹서버에 많은 데이터를 전달하기 위해서는 Post 방식을 사용하는 것이 바람직함
    Session과 Cookie
- **Session / Cookie**
  - 현재 우리가 인터넷에서 사용하고 있는 HTTP프로토콜은 연결 지향적인 성격을 버렸기 때문에 새로운 페이지를 요청할 때마다 새로운 접속이 이루어지며 이전 페이지와 현재 페이지 간의 관계가 지속되지 않는다. 이에 따라 HTTP프로토콜을 이용하게 되는 웹사이트에서는 웹페이지에 특정 방문자가 머무르고 있는 동안에 그 방문자의 상태를 지속시키기 위해 쿠키와 세션을 이용한다.
  - Session
    - 특정 웹사이트에서 사용자가 머무르는 기간 또는 한 명의 사용자의 한번의 방문을 의미
    - Session에 관련된 데이터는 **Server 저장**
    - 웹 브라우저의 캐시에 저장되어 브라우저가 닫히거나 서버에서 삭제시 사라짐
    - Cookie에 비해 보안성 좋음
  - Cookie
    - 사용자 정보를 유지할 수 없다는 HTTP의 한계를 극복할 수 있는 방법
    - 인터넷 웹 사이트의 방문 기록을 남겨 사용자와 웹 사이트 사이를 매개해 주는 정보
    - Cookie는 인터넷 사용자가 특정 웹서버에 접속할 때, 생성되는 개인 아이디와 비밀번호, 방문한 사이트의 정보를 담은 임시 파일로써,
      Server가 아닌 **Client에 텍스트 파일로 저장** 되어 다음에 해당 웹서버를 찾을 경우 웹서버에서는 그가 누구인지 어떤 정보를 주로 찾았는지 등을 파악할 때 사용됨
    - Cookie는 Client PC에 저장되는 정보기 때문에, 다른 사용자에 의해서 임의로 변경 가능(정보 유출 가능, Session보다 보안성이 낮은 이유)
  - Q. 보안성이 낮은 Cookie 대신 Session을 사용하면 되는데 안하는 이유는?
    - A. 모든 정보를 Session에 저장하면 Server의 메모리를 과도하게 사용하게 되어 Server에 무리가 감
- **Thread / Process**
  - Thread : 프로세스내 작업 단위
  - Thread 단점
    - 교착상태(다중프로그래밍 체제에서 하나 또는 그 이상의 프로세스가 수행 할 수 없는 어떤 특정시간을 기다리고 있는 상태)에 빠질 수 있음
  - Process(프로세스) : 운영체제에서 실행중인 하나의 프로그램(하나 이상의 쓰레드를 포함한다.)
  - Thread와 Process 차이
    - 스레드는 프로세스 내에서 실행되는 세부 작업 단위로 여러 개의 스레드가 하나의 프로세스를 이루게 됨
- **Singleton Design Pattern(싱글톤 디자인 패턴, 싱글톤 패턴)**
  - 클래스 인스턴스가 하나만 만들어지도록 하고, 그 인스턴스에 대한 전역 접근 제공
  - app이 시작 될 때 클래스가 최초로 한번만 메모리를 할당하고 그 메모리에 인스턴스를 만들어 사용.
  - 전역 인스턴스여서 다른 클래스 인스턴스가 데이터를 공유하기 쉬움. 인스턴스가 절대적으로 하나라는 것을 보증하고싶을 경우. 두 번째 이용시부터 객체 로딩 시간이 줄어 성능 개선.
  - 멀티쓰레드 환경에서 객체가 두개 이상이 되는 문제생김
    - 해결 1) synchronized : 동기화, volatile : 원자성 보장  / but, 성능에 안좋음
    - 해결 2) 객체를 프로그램 시작과 동시에 초기화하는 방법
    - 해결 3) 별도의 static class에서 초기화를 해서 가지고있음
- **Stack / Queue**
  - Stack
    - Last In First Out
    - pop, push
  - Queue
    - First In First Out
    - 프로세스 처리, CPU 관리, 프린터 큐등에 사용
- **MVC패턴**
  - model, view, controller로 이루어진 패턴
    - model : 논리적데이터 기반 구조 표현
    - view : 사용자 인터페이스 내의 구성요소들을 표현 (사용자에게 보여지는 화면)
    - controller : 모델과 뷰내의 클래스 간의 정보교환
  - (장) 코드의 가독성, 확장성
  - (단) 설계 시간이 오래걸리고 숙련된 개발자가 필요하며, model과 view의 완벽한 분리가 어렵다(의존적)
- **MVP 패턴**
  - model과 view의 의존성 분리
  - 모델(Model)
    - MVC와 동일
  - 뷰(View)
    - 액티비티/프래그먼트가 이제 뷰의 일부로 간주됨
    - 따라서 이들이 서로에게 연관되는 자연스러운 현상을 극복할 필요가 없음. 액티비티가 뷰 인터페이스를 구현해서 프리젠터가 코드를 만들 인터페이스를 갖도록 하는 것이 좋음
  - Presenter
    - (view에서 요청한 정보를 model로부터 가공하여 view로 전달)
    - 본질적으로는 MVC의 컨트롤러와 같지만, 뷰에 연결되는 것이 아니라 그냥 인터페이스라는 점이 MVC와 다름
  - (단) view와 presenter가 강한 의존성을 가짐
    - 유지 보수 : 컨트롤러처럼 프리젠터에도 시간이 지남에 따라 추가 비즈니스 로직이 모이는 경향이 있음. 시간이 흐른 후 개발자는 거대하고 다루기 어려운데다 문제가 발생하기 쉽고 분리하기도 어려운 프리젠터를 발견됨.

## 기타
- [고무오리 문제 해결법🐤](http://wikibook.co.kr/article/rubber-duck-problem-solving/)
  - 고무오리를 통해 문제를 해결한다는 방법의 핵심이 진지한 태도로 상상 속의 사람이나 사물을 향해 철저하고 상세한 질문을 던지는 데 있다.



---
refer to
- [[면접]웹 프로그래머(JAVA, JSP) 면접 예상 질문](http://hahahoho5915.tistory.com/16?category=660341)
- [[면접] IT 신입 개발자 기술 면접 대비 정리](http://dailyddubby.blogspot.com/2018/05/111-it.html)
