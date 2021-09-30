---
laout : single
title: "Java 시작하기"
---

# 개발 환경 구축을 위한 Java 설치 및 환경 변수 설정

## 개발자의 종류
JAVA 언어를 학습하기 이전에 IT 개발자는 어떤 종류가 있는지를 알아보려 합니다.
- Front-end 개발자
  - 사용자에게 보여지는 화면을 개발합니다.
  - 주로 HTML, CSS, JavaScript를 사용합니다.
  - 최근 표준화된 HTML5에 맞춰 모바일과 PC모두 대응하는 반응형 웹이 유행한다고 합니다.
<br>
- Back-end 개발자
  - 웹 상에서 사용되는 웹페이지가 원하는 기능을 하도록 DB와 API서버 개발을 맡습니다.
  - Front-end 지식 뿐만 아니라 Java, Python, MySQL 등 다양한 기술이 요구 된다고 합니다.
<br>
- Full-stack 개발자
  - 위의 Front-end & Back-end를 모두 다룰 수 있는 개발자를 말합니다.
  - Full-stack 개발자라고 말하는 사람은 자신의 분야가 확립되지 않은 개발자이거나 경력이 긴 작은기업 대표일 가능성이 높다고 합니다.

## Java 설치하기
- Java 플랫폼 종류
  - Java SE(standard Edition)    : 자바의 기본 개발 환경
  - Jvav EE(Enterprise Edition)  : 서버 기반 프로그램의 개발 환경
  - Java ME(Micro Edition) : 모바일 및 임베디드 시스템의 개발 환경

ORACLE 사이트에서 JAVA SE 1.8ver을 다운로드 & 설치
<img src="/assets/post_photo/Java_Download.JPG" width="100%">
- Java 1.11ver 버전 이후엔 ORACLE에서 유료화를 진행하였다고 한다. Java 1.8ver버전은 무료이기 때문에 1.8ver을 쓰자.
- Java 1.8ver은 JDK(Java development kit), JRE(Java Runtime Environment)가 구분되어 있는데 1.11ver부터는 JDK로 통합되었다고 한다.

## 환경 변수 설정
Java 설치 후 환경변수를 설정해야 원활하게 개발을 진행할 수 있다.
- '내컴퓨터 설정 > 고급 설정 > 환경 변수 > 시스템 변수'에서 설정을 진행한다

아래와 같이 시스템 변수를 생성한다. 경로는 Java가 설치된 폴더에서 JDK 폴더 경로를 설정해주면된다.( Java 1.8ver은 JDK / JRE 두 폴더로 나누어져 생성된다. )

<img src="/assets/post_photo/system_setting.jpg" width="90%">


이후 path의 환경 변수 편집에서 아래와 같이 변수를 새로 생성후 맨위로 올린다.
<img src="/assets/post_photo/path.jpg" width="90%">


'시작프로그램-CMD'을 실행하여 명령 프롬프트에서 Java version 확인이 가능하다.
> 〉java -version
<img src="/assets/post_photo/java_version.jpg" width="90%">

## eclipse 설치
Java 프로그래밍을 하는 툴은 eclipse를 사용하였고 홈페이지에서 쉽게 다운로드 & 설치가 가능하다.
<img src="/assets/post_photo/eclipse.JPG" width="90%">
