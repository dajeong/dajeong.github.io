---
title: Java SE, Java EE, Java ME, JavaFX 정리
updated: 2018-02-01 23:37
---


자바를 공부하면서 *최소한 내가 자바의 어떤 플랫폼으로 개발하고 있는지는 알아야지!* 라고 생각하며 대충 알고 있던 내용을 정리해 보고자 합니다.

출처는 [이 곳](http://javawebaction.blogspot.kr/2014/07/introuction-and-difference-of-java-se-java-ee-java-me-javafx.html)!! 입니다. (제 글은 허접한 해석이 많을 수 있습니다. 원 글을 보시면 더욱 도움이 되실겁니다 !)

<br>
<div class="divider"></div>
<br>

이 글에서는 Java SE, Java EE, Java ME and JavaFX 의 차이점에 대해 얘기합니다.
많은 SW 개발자(특히 자바 개발자)들이 이들의 차이점과 이들 서로의 관계에 대해 알지 못합니다.
SE는 데스크톱 애플리케이션 개발을 위해, EE는 웹 기반 애플리케이션 개발을 위해, ME는 모바일 애플리케이션 개발을 위해 디자인 되었습니다.
복잡한 비즈니스 애플리케이션은 웹 인터페이스와 데스크톱 클라이언트 그리고 모바일 클라이언트로 구성될 수 있고 이와 같은 경우를 앞서 설명한 플랫폼을 결합하여 개발 할 수 있습니다.


### Java SE
SE는 Standard Edition의 약자 입니다. 대부분의 자바 데스크톱 애플리케이션을 개발하는데 쓰이며, 자바 [core API](https://docs.oracle.com/javase/8/docs/api/)로써 사용됩니다.
기본적인 자바의 데이터 타입과 보안, 데이터베이스 액세스, GUI(Graphical User interface) 개발, 네트워킹 애플리케이션 개발 등등 과 관련 객체들도 포함합니다.
Java SE는 자바 기반 애플리케이션 개발을 위한 가상 머신 (VM), 개발 도구, 여러가지 클래스 라이브러리, 배포 기술로 구성됩니다.

### Java EE
EE는 Enterprice Edition의 약자 입니다. SE 플랫폼 기반으로 구축되었고, [애플리케이션 서버와 웹 서버](https://www.javaworld.com/article/2077354/learn-java/app-server-web-server-what-s-the-difference.html)에서 실행되는 웹 기반 애플리케이션을 개발하기위한 플랫폼입니다. 대규모, 확장 가능, 신뢰성 있는, 다중 계층이고 보안 네트워크를 포함하는 애플리케이션 개발을 위한 런타임 환경의 여러 API 들을 제공합니다. Java EE 기술로 Java Servlet, JSP, JSF, Primefaces, Oracle ADF가 있습니다.


### Java ME
ME는 Micro Edition의 약자 입니다. 휴대폰 같이 작은 규모의 장치에서 동작하는 애플리케이션 개발을 위한 플랫폼 입니다. 다양한 휴대폰 애플리케이션과 게임 개발에 사용됩니다. 
유명한 채팅 앱인 [Whatsapp](https://web.whatsapp.com/) 또한 Java ME로 개발되었습니다. Java ME로 개발된 애플리케이션은 다양한 모바일 폰 운영체제(Nokia Symbian, Android, Iphone and window phone etc)에서 돌아갑니다.
Java ME로 개발된 애플리케이션은 Java EE 플랫폼 서비스의 클라이언트로 사용될 수 있습니다.


### JavaFx
JavaFx는 강력한 자바 기반의 UI(User Interface) 플랫폼입니다. 이 플랫폼을 이용하여 경량 UI API를 사용하여 대규모 데이터 기반 비즈니스 애플리케이션과 풍부한 인터넷 애플리케이션을 개발할 수 있습니다. 
JavaFx로 개발된 애플리케이션은 고성능 클라이언트와 최신 인터페이스를 위해 하드웨어 가속 그래픽 및 미디어 엔진을 사용합니다.
JavaFx 애플리케이션 또한 Java EE 서비스의 클라이언트로 사용될 수 있습니다.
