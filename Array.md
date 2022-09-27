# **배열**
배열은 연관된 데이터를 모아서 관리하기 위해서 사용하는 데이터 타입으로 변수가 하나의 데이터를 저장하기 위한 것이라면 배열은 여러 개의 데이터를 저장하기 위한 것이라고 할 수 있습니다.  
<br><br>


다음은 배열을 생성하는 방법입니다.
```
public class DefineDemo {
 
    public static void main(String[] args) {
 
        String[] classGroup = { "최민욱", "박준서", "안강호", "오진서" };
 
    }
 
}
```
String[] classGroup에서 classGroup은 배열이 담길 변수의 이름입니다. String[]은 classGroup에 담을 배열에 담길 데이터의 타입이 문자열의 배열이라는 의미이고 배열을 선언할 때는 데이터 타입 뒤에 []를 붙여야 합니다. 만약 []가 없다면 classGroup는 배열이 아니라 문자열 데이터 타입을 갖는 변수가 됩니다. 즉 배열에 소속될 데이터들은 중괄호 안에 위치하고 각각의 데이터들은 쉼표로 구분됩니다.  


<br><br>
아래의 코드는 배열에 담겨있는 데이터를 출력하는 방법입니다.
```
public class GetDemo {
 
    public static void main(String[] args) {
        String[] classGroup = { "최민욱", "박준서", "안강호", "오진서" };
        System.out.println(classGroup[0]);
        System.out.println(classGroup[1]);
        System.out.println(classGroup[2]);
        System.out.println(classGroup[3]);
 
    }
 
}
```
<br><br>
실행결과는 다음과 같습니다.
```
최민욱
박준서
안강호
오진서
```
<br>
위와 같이 배열의 index 번호는 0번 부터 시작하며 배열을 생성할 때 중괄호 안에 적었던 순서대로 값이 저장되게 되는 것을 알 수 있습니다.

<br><br>

또한 배열은 다음과 같이 반복문과의 결합을 통해 효율적인 코드를 만들 수 있습니다.
```
public class ArrayLoopDemo {
 
    public static void main(String[] args) {
 
        String[] members = { "최민욱", "박준서", "안강호" };
        for (int i = 0; i < members.length; i++) {
            String member = members[i];
            System.out.println(member + "이(가) 상담을 받았습니다");
        }
 
    }
 
}
```

<br><br>
실행결과는 다음과 같습니다.
```
최민욱이(가) 상담을 받았습니다
박준서이(가) 상담을 받았습니다
안강호이(가) 상담을 받았습니다
```

<br>
다음과 같이 배열이라는 연관된 정보를 하나의 그룹으로 관리하기 위해서 반복문을 이용하면 효율적으로 코드를 짤 수 있어 반복문과 배열은 매우 밀접한 관계에 있다고 할 수 있습니다.

<br><br>

## **for-each**
배열의 내용을 탐색할 때 사용하는 for 문을 좀 더 간편하게 사용할 수 있습니다. 아래 코드를 보겠습니다.

```
public class ForeachDemo {
 
    public static void main(String[] args) {
        String[] members = { "최진혁", "최유빈", "한이람" };
        for (String e : members) {
            System.out.println(e + "이 상담을 받았습니다");
        }
    }
 
}
``` 
<br>
위의 예제는 for-each를 사용하지 않은 for 문과 실행결과는 동일하지만 문법적으로는 간결해졌습니다.

<br>
for-each 문을 사용하면 따로 for 문의 조건문을 입력할 필요 없이 배열 members의 값을 변수 e에 담아서 중괄호 구간 안으로 전달해주어 기준값을 증가시키는 등의 반복적인 작업을 내부적으로 감추어 보다 쉬운 유지보수가 가능하게 됩니다.