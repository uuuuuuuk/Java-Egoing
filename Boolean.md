# **비교와 Boolean**

## **Boolean** 
불린(Boolean)은 참과 거짓을 의미하는 데이터 타입으로 bool이라고도 부릅니다. 불린은 정수나 문자와 같이 하나의 데이터 타입인데, **참을 의미하는 true** 와 **거짓을 의미하는 false** 두 가지의 값을 가지고 있습니다. 아래는 비교 연산자들에 대한 설명입니다.
<br><br>
## **비교 연산자**
프로그래밍에서 비교란 주어진 값들이 같은지, 다른지, 큰지, 작은지를 구분하는 것을 의미합니다. 이때 비교 연산자를 사용하는데 비교 연산자의 결과는 true나 false 중의 하나입니다. true는 비교 결과가 참이라는 의미이고, false는 거짓이라는 뜻입니다. 
<br><br>
## **1. ==** 
좌항과 우항을 비교해서 서로 값이 같다면 true 다르다면 false가 됩니다. **" = "** 이 하나인 대입 연산자와는 다릅니다.  
<br><br>
아래는 **" == "** 에 대한 코드 입니다.
```
public class EqualDemo {
 
    public static void main(String[] args) {
        System.out.println(1==2);           //false
        System.out.println(1==1);           //true
        System.out.println("one"=="two");   //false
        System.out.println("one"=="one");   //true
    }
 
}
```
<br><br>
## **2. !=**
**" ! "** 는 부정을 의미합니다. 즉, '같다'의 부정은 '같지 않다'이므로 이것을 기호로는 **" != "** 로 표시합니다. 아래의 코드는 != 에 대한 코드인데 == 와 정반대의 결과를 보여줍니다.
<br>
```
public class NotDemo {
 
    public static void main(String[] args) {
        System.out.println(1!=2);           //true
        System.out.println(1!=1);           //false
        System.out.println("one"!="two");   //true  
        System.out.println("one"!="one");   //false
    }
     
}
```
<br><br>
## **3. >**
좌항이 우항보다 크다면 참, 그렇지 않다면 거짓임을 알려주는 연산자입니다. '<'는 반대의 의미로 작다면 참, 그렇지 않다면 거짓을 출력합니다.
<br>
```
public class GreaterThanDemo {
 
    public static void main(String[] args) {
        System.out.println(10>20);       //false
        System.out.println(10>2);            //true
        System.out.println(10>10);           //false
 
    }
 
}
```
<br><br>
## **3. >=**
좌항이 우항보다 크거나 같다면 참, 그렇지 않다면 거짓임을 알려주는 연산자입니다. **" <= "** 는 반대의 의미로 작거나 같다면 참, 그렇지 않다면 거짓을 출력합니다.
```
public class GreaterThanOrEqualDemo {
 
    public static void main(String[] args) {
 
        System.out.println(10 >= 20); // false
        System.out.println(10 >= 2); // true
        System.out.println(10 >= 10); // true
 
    }
 
}
```
<br><br>
## **4. .equals**
.equals는 **문자열을 비교할 때 사용하는 메소드** 이지만 연산자로 이해해도 무방합니다.

```
public class EqualStringDemo {
 
    public static void main(String[] args) {
        String a = "Hello world";
        String b = new String("Hello world");
        System.out.println(a == b);
        System.out.println(a.equals(b));
    }
 
}
```
해당 코드에서는 변수 a와 b에 각각 문자열을 생성해서 저장했습니다. 변수 b에 문자열을 만드는 방법은 생성자를 이용하고 있는데 먼저 코드의 결과는 false와 true입니다. == 은 두개의 데이터 타입이 동일한 객체인지를 알아내기 위해서 사용하는 연산자이기 때문에 b에 담긴 객체와는 일치하지 않는 것인데 이를 보완하는 비교 방법이 equals이고 이를 이용해서 **서로 다른 객체들간에 값이 같은지** 를 비교할 수 있습니다.