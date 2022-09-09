# **숫자와 문자**
데이터 형 중 가장 많이 사용되는 데이터 타입(data type)은 **숫자**와 **문자**일 것입니다.

그렇다면 자바에서 이 숫자와 문자는 어떻게 표현할 수 있을까요?  
.  
.  
.  
## **1. 숫자**
자바에서 숫자를 출력하여 표현하는 방법에는 몇가지 규칙이 있습니다.
<br><br>
- 자바에서는 따옴표가 없는 숫자는 숫자로 인식합니다.  

```
System.out.println(1+2); --> 실행결과 : 3
System.out.println(1.2+1.3); --> 실행결과 : 2.5

System.out.println(5-3); --> 실행결과 : 2 
```
<br>

- 곱하기를 할 때는 *(에스터리스크) 를 사용합니다.  
```
System.out.println(2*5); --> 실행결과 : 10 
```
<br>

- 나누기를 할 때는 /(슬래쉬) 를 사용합니다.  
```
System.out.println(6/2); --> 실행결과 : 3 
```
<br>

- 나머지 값을 구할 때는 %(퍼센트) 를 사용합니다.  
```
System.out.println(8/3); --> 실행결과 : 2 
```
<br>

## **2. 문자와 문자열**
자바는 **문자(Character)** 와 **문자열(String)** 을 구분합니다. 여기서 문자는 한 글자를 의미하고, 문자열은 여러 개의 문자가 결합한 것을 의미한다. 다음은 자바에서의 문자와 문자열의 규칙입니다. 
<br><br> 
- 자바에서 문자는 작은 따옴표로 감싸야합니다.   
```
System.out.println('생');
``` 
<br>

- 자바에서 문자열은 큰 따옴표로 감싸야합니다.  
```
System.out.println("생활코딩");
``` 
<br>

- 만약 문자열을 작은 따옴표로 감싸면 에러가 발생하게 됩니다.  
```
System.out.println('생활코딩');
``` 
<br>

- 만약 하나의 문자를 큰 따옴표로 감싸게 되어도 오류가 발생하지 않습니다. 하나의 문자도 문자열이 될 수 있기 때문입니다.  
```
System.out.println("생");
``` 
<br>

## **2-1 이스케이프**
만약 문자열 안에 큰 따옴표를 넣고 싶다면 어떻게 해야 할까요?  <br><br>
아래와 같이 코드를 작성하게 되면 오류가 발생할 것입니다.
```
System.out.println("egoing said "Welcome programming world"");
```
<br>

이럴떄는 다음 코드와 같이 사용하면 됩니다.
```
System.out.println("egoing said \"Welcome programming world\"");
```
이렇게 ( \ ) 를 사용하게 되면 ( " " ) 를 문자를 끝내는 구분자의 역할이 아닌 단순히 문자로 구분될 수 있게 하는데 이러한 기법을 바로 **이스케이프(escape)** 라고 합니다.
<br><br>

## **2-2 여러줄의 표시**
만약 한 코드 줄을 작성하더라도 그 출력을 각각 다르게 여러 줄에서 표시하려면 어떻게 해야할까요? <br><br>
이럴때는 줄을 바꾸고 싶은 글자 사이에 **\n** 을 사용하며 이를 코드로 표현하면 다음과 같습니다.  
```
System.out.println("HTML\nCSS\nJavaScript\n");
```
<br>

## **2-3 문자의 연산**
만약 우리가 **" 안녕하세요 "** 라는 문자열을 작성하려면 어떻게 코드를 작성해야 할까요? <br><br>
단순히 코드를  
```
System.out.println("안녕하세요");
```
라고 작성해도 되겠지만 이를 다르게 표현 할 수도 있습니다. <br><br>
바로 문자와 문자를 더하는 방법인데 이는 다음과 같이 표현 가능합니다.  
```
System.out.println("생활"+"코딩");
``` 
<br>
우리가 숫자를 더할 때 **" + "** 를 사용해 숫자를 계산했던 것 처럼 문자를 합치려고 할 때 **" + "** 를 사용하면 문자, 또는 문자열 여러개를 합쳐 하나의 문자열을 만들게 됩니다.