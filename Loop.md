# **반복문**
반복문은 말 그대로 **반복적인 작업을 보다 효율적으로 실행하기 위해 만들어진 문법** 입니다.  
<br><br>
## **1. while**
while은 ~할 때 동안 이라는 뜻을 가진 반복문 중 하나로 

while 문의 형식은 다음과 같습니다.
```
while(조건){
    반복 실행 영역
}
```  
<br><br><br>
해당 방식으로 코드를 하나 만들어보겠습니다.

```
public class WhileDemo {
 
    public static void main(String[] args) {
        while (true) {
            System.out.println("Coding Everybody");
        }
 
    }
 
}
```
아마 해당 코드는 " Coding Everybody " 라는 출력이 무한 반복 될 것 입니다. 이는 조건이 무조건적으로 참이기 때문입니다. 그렇다면 옳게 된 while 문의 사용법을 보겠습니다.  

<br><br>
```
int i = 0;

while(i<10){         
    System.out.println("Coding Everybody");

    i++;
}
```
해당 코드에는 0으로 초기화 되어있는 i 라는 변수에 " 10보다 작을 때 동안 " 이라는 조건이 달려있고 무한반복을 방지 하기 위해 중괄호의 마지막에 i 의 값을 1씩 증가시키는 단항연산자 **" ++ "** 를 사용하였습니다.

<br><br>
## **2. for**
while문을 보면 반복의 횟수를 지정하기 위해서 while문 외부에 변수 i의 값을 초기화하고, while문 안에서 i의 값을 증가시키고 있습니다. 이것은 코드를 산만하게 할 수 있는데 반복문에서 자주 사용하는 이러한 패턴을 문법적인 형태로 만든 것이 for문입니다.

for 문의 형식은 다음과 같습니다.
```
for(초기화; 종료조건; 반복실행){
    반복적으로 실행될 구문
}
```
<br><br>
이렇게 for 문의 괄호 안에는 총 3개의 부품으로 구성되는데

이를 각각 세부적으로 보면

**초기화** : 반복문이 실행될 때 1회 실행된다.

**종료조건** : 초기화가 실행된 후에 종료조건이 실행된다.

**반복 실행** : 종료조건의 값이 false일 때까지 반복문의 중괄호 구간의 코드가 반복 실행된다.
중괄호 구간의 실행이 끝나면 반복 실행이 실행된다. 일반적으로 이 곳에 i++와 같이 변수를 증가시키는 로직이 위치하고, 이것이 실행된 후에 종료조건이 실행된다. 종료조건이 false가 될 때까지 이 과정이 반복된다.


<br><br>
다음은 위의 while 문을 for 문으로 표현한 코드입니다.
```
public class ForDemo {
 
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            System.out.println("Coding Everybody ");
        }
 
    }
 
}
```
<br><br>

## 3. **break, continue**
만약 반복문을 실행하다가 **결과값을 중지시키거나 일부분을 건너뛰고 싶다면** 어떻게 해야할까요?? 이럴 때 사용하는 도구가 바로 **break**, **continue** 입니다.    
<br><br>
## **3-1. break**
break 는 **반복문을 중단** 시키고 싶을 때 사용하는 도구입니다.

아래의 코드를 보겠습니다.
```
public class BreakDemo {
 
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            if (i == 5)
                break;
            System.out.println("Coding Everybody ");
        }
 
    }
 
}
```  
<br><br>

코드의 실행 결과는 다음과 같습니다.
```
coding everybody 0
coding everybody 1
coding everybody 2
coding everybody 3
coding everybody 4
```
원래 위의 코드라면 for 문에서 봤던 것 처럼 " Coding Everybody " 라는 실행문이 10번 출력되어야 하지만 i 가 증가 되다가 i = 5 일때 코드가 중단되는 조건문을 만나 종료되기 때문에 다음과 같은 결과가 출력된 것입니다.

<br><br>
## **3-2. continue**
그럼 **실행을 즉시 중단하면서 반복은 지속해가게 하려면** 어떻게 해야 할까요?? 이럴 때 사용하는 도구가 바로 **continue** 입니다.

아래의 코드를 보겠습니다.
```
public class ContinueDemo {
 
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            if (i == 5)
                continue;
            System.out.println("Coding Everybody " + i);
        }
 
    }
 
}
```
<br><br>

코드의 실행 결과는 다음과 같습니다.
```
Coding Everybody 0
Coding Everybody 1
Coding Everybody 2
Coding Everybody 3
Coding Everybody 4
Coding Everybody 6
Coding Everybody 7
Coding Everybody 8
Coding Everybody 9
```
같은 코드에 break 와 continue 만 변경된 모습이지만 코드의 결과값은 완전히 다른 값을 출력합니다. 그 이유는 i = 5 일때 continue 문이 실행되어 건너뛰고 바로 i = 6 부터 실행되기 때문입니다. 

<br><br>
## **4. 반복문의 중첩**
반복문 안에는 반복문이 나타날 수 있습니다. 다음 예제는 반복문 속 반복문, 일명 **중첩 for** 문을 기록한 코드입니다.
```
public class LoopDepthDemo {
 
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            for (int j = 0; j < 10; j++) {
                System.out.println(i + "" + j);
            }
        }
 
    }
 
}
```
다음과 같이 코드를 작성하면 첫번째 for 문의 식이 참이면 두번째 for 문으로 넘어가 두번째 for 문이 끝까지 출력된 후 다시 첫번째 for 문으로 넘어가 1 이 증가되는 것이 반복되어 총 00 부터 99 까지 100번을 출력하게 됩니다.