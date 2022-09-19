# **반복문**
반복문은 말 그대로 반복적인 작업을 보다 효율적으로 실행하기 위해 만들어진 문법입니다.  
<br><br>
## **1. while**
while은 ~할 때 동안 이라는 뜻을 가진 반복문 중 하나로 while 문의 형식은 다음과 같습니다.
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
    System.out.println("Coding Everybody"+i);

    i++;
}
```
해당 코드에는 0으로 초기화 되어있는 i 라는 변수에 " 10보다 작을 때 동안 " 이라는 조건이 달려있고 무한반복을 방지 하기 위해 중괄호의 마지막에 i 의 값을 1씩 증가시키는 단항연산자 " ++ " 를 사용하였습니다.

