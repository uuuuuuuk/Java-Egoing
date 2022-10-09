# **조건문**
조건문이란 **주어진 조건**에 따라서 애플리케이션을 다르게 동작하도록 하는 것으로 프로그래밍의 핵심 중의 하나라고 할 수 있습니다.  
<br><br>
## **1. if**
![Untitled](./img/if.png) <br>
위 사진은 if 문의 문법 구조를 나타낸 것입니다. if 문 뒤의 괄호를 **" if 절 "** 이라고 부르고 이 if 절의 내용이 **참(True)** 일 경우 중괄호 안의 절이 실행되고 거짓이라면 실행되지 않습니다. 아래는 if 문을 사용한 코드입니다.
<br><br>
```java
public class Condition1Demo {
 
    public static void main(String[] args) {
        if(true){
            System.out.println("result : true");
        }
    }
}
```
해당 코드의 실행결과는 **" result : true "** 입니다. if 절 안에 참(True)이 왔기 때문입니다.
<br><br>
```java
if(false){
    System.out.println("result : true");
}
```
반대로 if 절 안의 괄호가 거짓(False) 일 때는 중괄호 안이 실행되지 않아 아무것도 출력되지 않습니다.  
<br><br>
```java
public class Condition2Demo {
 
    public static void main(String[] args) {
        if (true) {
            System.out.println(1);
            System.out.println(2);
            System.out.println(3);
            System.out.println(4);
        }
        System.out.println(5);
    }
 
}
```
해당 코드의 실행 결과는 12345입니다. if 문 안의 코드를 실행한 후 중괄호를 빠져나와 5를 출력했기 때문입니다.  
<br><br>
```java
if(false){
    System.out.println(1);
    System.out.println(2);
    System.out.println(3);
    System.out.println(4);
}
System.out.println(5);
```
반대로 해당 코드는 5만 출력할 것 입니다. if 절이 거짓이므로 중괄호를 실행시키지 못하고 빠져나와 5만을 출력했기 때문입니다.

<br><br>
## **1-1. else**
![Untitled](./img/else.png) <br>
else문은 if 문 만으로는 해결되지 않는 더 복잡한 상황을 처리하는데 사용되는 절입니다.

<br><br>
```java
public class Condition3Demo {
 
    public static void main(String[] args) {
        if (true) {
            System.out.println(1);
        } else {
            System.out.println(2);
        }
 
    }
 
}
```
해당 코드의 결과는 1 입니다. if 절이 참이기 때문에 else 절은 출력하지 않기 때문입니다.

<br><br>
```java
if(false){
    System.out.println(1);
} else {
    System.out.println(2);
}
```
해당 코드의 결과는 2 입니다. if 절이 거짓이므로 else 문만이 출력되기 때문입니다.

<br><br>
## **1-2. if-else**
![Untitled](./img/if-else.png) <br>
if-else 절은 else 절 보다도 조건문을 더 자유롭게 제어할 수 있게 도와주는 조건문입니다.  
<br><br>
```java
public class ElseDemo {
 
    public static void main(String[] args) {
        if (false) {
            System.out.println(1);
        } else if (true) {
            System.out.println(2);
        } else if (true) {
            System.out.println(3);
        } else {
            System.out.println(4);
        }
 
    }
 
}
```
다음 코드의 결과는 2입니다. if 문에서 거짓이므로 else-if 문으로 넘어간 후 2번에 else-if에서 참을 찾아 2라는 값을 출력했기 때문입니다. 참(True)의 값이 여러개더라도 처음 참의 실행문만 실행합니다. 

<br><br>
## **1-3. 중첩 if**
하나의 코드에서 2번, 또는 여러번의 검사를 실행해야 한다면 어떻게 해야할까요? 이럴 때 사용하는 것이 바로 중첩 if 문 입니다. 아래 코드를 보겠습니다.

```java
public class ifinif {
    public static void main(String[] args) {
        String id = "id"
        String password = "password"
        if (id = "id") {
            if (password = "password") {
                System.out.println("right");
            } else {
                System.out.println("wrong");
            }
 
        } else {
            System.out.println("wrong");
        }
    }
}
``` 
해당 코드에서는 문자열 변수인 id , password 가 모두 옳은 값이여야만 **" right "** 를 출력하고 나머지는 모두 " wrong " 을 출력하게 됩니다. 이렇게 **if 문 안에 if문을 넣어 조건을 여러번 검수 하는 방법** 을 중첩 if 라고 합니다.  

<br><br>
## **2. switch**
조건문의 대표적인 문법은 if 문 이지만 사용빈도는 적고, 조건이 많은 경우에는 switch 문을 사용해 로직을 보다 명료하게 표현할 수 있습니다.  
<br>
```java
public class SwitchDemo {
 
    public static void main(String[] args) {
         
        System.out.println("switch(1)");
        switch(1){
        case 1:
            System.out.println("one");
        case 2:
            System.out.println("two");
        case 3:
            System.out.println("three");
        }
         
        System.out.println("switch(2)");
        switch(2){
        case 1:
            System.out.println("one");
        case 2:
            System.out.println("two");
        case 3:
            System.out.println("three");
        }
         
        System.out.println("switch(3)");
        switch(3){
        case 1:
            System.out.println("one");
        case 2:
            System.out.println("two");
        case 3:
            System.out.println("three");
        }
 
    }
 
}
```
<br><br>
실행결과는 다음과 같습니다.
```
switch(1)
one
two
three
switch(2)
two
three
switch(3)
three
```
<br>
코드를 해석해보면 먼저 첫번째 switch 문에서는 1이 입력되었으므로 case 1에 해당하는 로직 이후의 모든 case들이 실행되고 두번째 switch 문에서는 2부터, 
세번째 switch 문에서는 3부터 실행되므로 해당 결과가 나온 것입니다.
<br><br>
그렇다면 다음과 같이 코드를 바꿔보겠습니다.

```java
public class SwitchDemo {
 
    public static void main(String[] args) {
         
        System.out.println("switch(1)");
        switch(1){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        }
         
        System.out.println("switch(2)");
        switch(2){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        }
         
        System.out.println("switch(3)");
        switch(3){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        }
 
    }
 
}
```
<br><br>
다음코드의 결과는 다음과 같습니다.
```
switch(1)
one
switch(2)
two
switch(3)
three
```
<br>

실행결과가 다음과 같이 나온 이유는 조건문에서 사용할 수 있는 **" break "** 를 만나면 switch 문의 실행이 즉시 중지되기 때문입니다.  
<br><br>
이번에는 switch 문에서 사용하는 default: 를 사용해 조금 전의 코드를 변형해보겠습니다.
```java
public class SwitchDemo {
 
    public static void main(String[] args) {
         
        System.out.println("switch(1)");
        switch(1){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        default:
            System.out.println("default");
            break;
        }
         
        System.out.println("switch(2)");
        switch(2){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        default:
            System.out.println("default");
            break;
        }
         
        System.out.println("switch(3)");
        switch(3){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        default:
            System.out.println("default");
            break;
        }
         
        System.out.println("switch(4)");
        switch(4){
        case 1:
            System.out.println("one");
            break;
        case 2:
            System.out.println("two");
            break;
        case 3:
            System.out.println("three");
            break;
        default:
            System.out.println("default");
            break;
        }
 
    }
 
}
```
<br><br>
다음코드의 결과는 다음과 같습니다.
```
switch(1)
one
switch(2)
two
switch(3)
three
switch(4)
default
```
<br><br>
실행결과를 보게 되면 마지막 실행은 default 가 나오게 되는데 이는 주어진 케이스가 없는 경우 실행되는 default 문 때문이다.