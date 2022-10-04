# **메소드**
메소드는 재사용할 수 있는 코드의 집합을 의미합니다.

클래스에서 메소드를 작성하여 사용하는 이유는 중복되는 코드의 반복적인 프로그래밍을 피할 수 있기 때문입니다.

또한, 모듈화로 인해 코드의 가독성도 좋아집니다.

그리고 프로그램에 문제가 발생하거나 기능의 변경이 필요할 때도 손쉽게 유지보수를 할 수 있게 됩니다.

<br><br>

## **메소드의 형식과 선언**
메소드는 사실 자바를 처음 시작했을 때부터 사용되고 있었습니다.

![Untitled](./img/method.png)

이것이 메소드의 기본 형식입니다. 나머지는 아래 코드를 보겠습니다.

<br><br>
```java
public class MethodDemo1 {
    public static void numbering() {
        int i = 0;
        while (i < 10) {
            System.out.println(i);
            i++;
        }
    }
 
    public static void main(String[] args) {
        numbering();
    }
}
```
<br><br>
결과는 아래와 같습니다.
```
0
1
2
3
4
5
6
7
8
9
```