# **연산자**
연산자란 특정한 작업을 하기 위해서 사용하는 기호를 의미합니다. 연산자는 수행하려는 작업의 종류에 따라 **대입 연산자, 산술 연산자, 비교 연산자, 논리 연산자** 등이 있습니다.
<br><br><br>
## **1. 산술 연산자**
산술 연산자는 **수학적인 계산**에 사용되는 연산자 입니다.

프로그래밍에서 사용되는 산술 연산자의 기호는 다음과 같습니다.
<br><br>
|+|더하기|
|---|---|
|-|**빼기**|
|*|**곱하기**|
|/|**나누기**|
|%|**나머지**|

<br><br>
해당 기호들을 사용해 코드를 만들어 보겠습니다.

```
public class ArithmeticDemo  {
    public static void main(String[] args) {
        
        int result = 1 + 2;
        System.out.println(result);
  
        
        result = result - 1;
        System.out.println(result);
  
        
        result = result * 2;
        System.out.println(result);
  
        
        result = result / 2;
        System.out.println(result);
  
        
        result = result + 8;
        
        result = result % 7;
        System.out.println(result);
    }
}
``` 
<br>
결과는 아래와 같습니다.

```
3
2
4
2
3
```
<br>

이 코드를 해석해보면 먼저 정수형 데이터 타입 result 에 1 + 2, 즉 3이라는 값이 대입되어 출력되고 그 3이라는 값에 1을 뺀 2가 출력, 2에서 2를 곱한 4, 4에서 2를 나눈 2가 출력된 후 2에서 8을 더한 10에 나머지 연산 % 7을 사용해 7을 뺀 나머지 값인 3이 출력되게 되는 것입니다.
<br><br><br>
## **2. 형변환**
형변환은 말 그대로 변수가 가지고 있는 고유한 데이터 타입형을 **변경**한다는 말입니다. <br><br>아래 코드를 보겠습니다.

```
public class DivisionDemo {
      
    public static void main(String[] args) {
        int a = 10;
        int b = 3;
          
        float c = 10.0F;
        float d = 3.0F;
          
        System.out.println(a/b);
        System.out.println(c/d);
        System.out.println(a/d);
          
    }
  
}
```
<br>
결과는 아래와 같습니다.

```
3
3.3333333
3.3333333
```
<br>
첫 번째 실행결과는 정수와 정수를 나눈 것입니다. 3은 나머지의 몫이고 나머지는 0.3333333....이 남으나 정수는 소수점을 표현할 수 없으므로 정수만 표시된 것입니다.
<br><br>
두번째 결과는 실수와 실수간의 연산이 실행되므로 소수점인
0.3333333.... 까지 표현이 됩니다.
<br><br>
세 번째 결과는 정수에서 실수를 나눈 것입니다. 이 경우에는 암시적으로 형 변환이 일어나는데 이 때에는 정수가 실수가 되어 두번째 연산과 같은 실행결과가 됩니다.
<br><br><br>

## **3. 단항연산자**
1+2에서 사용한 연산자 **" + "** 는 이항 연산자이고, 좌항인 1과 우항인 2를 더해주는 작업을 하고 있습니다. 단항 연산자는 하나의 항을 대상으로 연산이 이루어지는 연산자로 다음은 자바에서 제공하는 단항 연산자들이다.
<br><br>
|+|양수를 표현합니다. 실제로는 사용할 필요가 없습니다.|
|---|---|
|-|**음수를 표현합니다.**|
|++|**증가 연산자로 항의 값을 1씩 증가 시킵니다.**|
|--|**감소 연산자로 항의 값을 1씩 감소 시킵니다.**|

<br><br>
해당 기호들을 사용해 코드를 만들어 보겠습니다.

```
public class PrePostDemo {
    public static void main(String[] args) {

        int i = 3;
        i++;

        System.out.println(i); // 4 출력

        ++i;
        System.out.println(i); 
        System.out.println(++i);
        System.out.println(i++); 
        System.out.println(i); 
    }
}
```
<br>
결과는 아래와 같습니다.

```
4
5
6
6
7
```
<br>

먼저 처음 i의 값은 3입니다. 다음 행에서 i++ 를 한 후 출력한 결과는 4가 되었고, 6행은 4행과 다르게 ++가 i 앞에 나왔지만 결과는 1이 증가한 5로 같습니다. 하지만 8행의 결과는 6이고, 9행의 결과값도 6입니다. ++i는 i의 값에 1이 더해진 값을 출력하는 것이고, i++는 이것이 속해있는 println에 일단 현재 i의 값을 출력하고, println의 실행이 끝난 후에 i의 값이 증가하는 특성이 있기 때문입니다.