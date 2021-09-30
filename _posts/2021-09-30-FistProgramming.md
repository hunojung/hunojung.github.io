---
laout : single
title: "Java 첫 프로그램 만들기"
---

# Java 프로그램 만들기 시작
Java를 배울 때 eclipse를 쓸 예정이지만 기본 개념을 잘 배워두자. 

## Java의 기본 작업 순서
1) *.java 형식의 소스파일 작성
2) javac *.java 명령으로 컴파일 진행 → *.class파일 생성됨
3) java * 으로 생성된 클래스파일 실행( .class는 입력하지 않아도 됨 )

- 메모장+터미널창으로 우선 테스트를 진행해본다.

메모장에 코드를 작성하고 Test01.java로 파일을 저장하자
( 파일명은 class 명과 같아야 한다! )
```
class Test01{
	public static void main(String args[]){
		System.out.println("hello");// hello 출력
	}
}
```
터미널 창에서 아래의 순서로 명령어를 입력해보자
```
〉javac Test01.java
〉java Test01
```
순서대로 javac를 이용해 컴파일 진행, Test01.class 파일 실행하였다.
이외에 명령어로 cd , dir이 있다.
```
〉cd c:\Test // 원하는 폴더 위치 설정
〉dir // 현재 폴더 내용 조회
```

<img src="/assets/post_photo/CMD_java.jpg" width="80%">
