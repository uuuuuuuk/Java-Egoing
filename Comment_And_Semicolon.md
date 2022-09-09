# **주석과 세미콜론**
## **1. 주석**
주석은 프로그래밍에서 어떠한 영향을 끼치는 것은 아니지만 자신이 한 프로그램을 오랜 기간 작성하고 있을 때 자신이 어떤 코드를 무슨 의도를 가지고 작성했는지 **기록해놓거나** 다른 사람과 협업을 할 때 이 코드가 어떤 코드인지, 또는 어떠한 코드를 **비활성화** 하고 싶을 때 사용되는 기능입니다. <br><br>
## **1-1 한줄 주석**
한줄 주석은 말 그대로 코드 내에 코멘트(Coment)를 넣거나 코드의 한 줄을 비활성화하고 싶을 때 사용하는 기능입니다. 
한줄 주석을 사용할 때는 **" // "** 를 사용합니다. <br>
```
int x = 10; // 이 코드는 정수형 변수 x 에 10을 대입한 코드입니다.
// int x = 10; --> 이 코드는 해석되지 않음 
int y = 20;
```
<br>

## **1-2 여러줄 주석**
여러줄 주석은 한줄 주석인 **" // "** 와는 달리 여러줄을 묶어 사용하고 **" /* */ "** 로 활성화 할 수 있습니다. 주로 코드를 비활성화 할 때만 사용되고 코멘트를 넣을 때는 사용하지 않습니다. <br>
```
int a = 10;
String y = "Hello";

/*
System.out.println(a); --> 이 코드는 해석되지 않음
System.out.println(y); --> 이 코드는 해석되지 않음
*/
```
<br>

## **2. 세미콜론**
**세미콜론 ( ; )** 은 문장(statement)의 끝을 의미합니다. 자바에서 문장의 끝에 세미콜론을 사용하지 않으면 컴파일 에러가 발생하게 됩니다.
```
int x = 10; double y = 20;
```
세미콜론을 사용하면 다음과 같이 여러개의 문장을 한줄에도 표현할 수 있습니다.
<br><br>
## **2-1. 세미콜론의 유래**
어떤 프로그래밍 언어를 사용하더라도 문장 끝에 마무리를 지을때 사용하는 것은 항상 세미콜론 입니다. 그런데 근본적으로 이것을 사용하는 이유는 무엇일까요? 

처음에 프로그램을 출력할 때 쓰는 프린터는 지금처럼 직사각형의 용지를 사용해서 여러 줄을 한번에 출력하는 것이 아니라, 줄자 혹은 카세트테이프처럼 한 줄만 인쇄할 수 있는 둘둘 말린 종이테이프에 인쇄되어 나왔었습니다. 따라서 출력을 하고 보면 모든 문장이 행의 구분이 없었으며, 이런 상황에서 행을 구분하기 위해 세미콜론을 매 행의 마지막에 박아주게 되었고, 이후에도 행을 구분할 때 세미콜론을 쓰는 것이 일종의 관례가 된 것입니다. 