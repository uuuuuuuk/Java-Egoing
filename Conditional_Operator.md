# **논리 연산자**
논리 연산자는 [Boolean](https://github.com/uuuuuuuk/Java-Egoing/blob/main/Boolean.md) 의 값을 결합해서 코드를 좀 더 간결하게 만들 수 있는 연산자입니다.  
<br><br>

## **1. &&**
&& 는 **좌항과 우항의 값이 모두 참(true)일 때 참이 되는 연산자**이고 **" And "** 라고 읽습니다. 

아래 코드를 보겠습니다.
```java
public class AndDemo {
 
    public static void main(String[] args) {
        if (true && true) {
            System.out.println(1);
        }
 
        if (true && false) {
            System.out.println(2);
        }
 
        if (false && true) {
            System.out.println(3);
        }
 
        if (false && false) {
            System.out.println(4);
        }
 
    }
 
}
```

다음 코드의 결과는 1 입니다. 첫 번째 if 문을 제외하면 나머지는 좌항과 우항이 모두 참이 아니기 때문입니다.

<br><br>

## **2. ||**
|| 는 **좌우항 중에 하나라도 참이라면 전체가 참이 되는 논리 연산자**이고 **" Or "** 라고 읽습니다.

아래 코드를 보겠습니다.
```java
public class OrDemo {
 
    public static void main(String[] args) {
        if (true || true) {
            System.out.println(1);
        }
        if (true || false) {
            System.out.println(2);
        }
        if (false || true) {
            System.out.println(3);
        }
        if (false || false) {
            System.out.println(4);
        }
 
    }
 
}
```
다음 코드의 결과는 123 입니다. 방금전 && 와는 다르게 첫 번째 if 문부터 세번째 if 문까지의 참(True) 에서 해당 if 문이 참이 되어 4번째 if 문을 제외한 나머지 실행문이 모두 실행되었기 때문입니다.

<br><br>

## **3. !**
! 는 **Boolean의 값을 역전시키는 역할**을 합니다. 즉 **true에 !를 붙으면 false가 되고 false에 !을 붙이면 true가 되고** 읽을 때는 부정의 의미로 **" not "** 이라고 읽습니다.

아래 코드를 보겠습니다.
```java
public class NotDemo {
 
    public static void main(String[] args) {
        if (!true) {
            System.out.println(1);
        }
        if (!false) {
            System.out.println(2);
        }
 
    }
 
}
```
다음 코드의 결과는 2입니다. **!** 를 통해 값이 역전되어 참이 거짓이 되고, 거짓이 참이 되었기 때문입니다.