---
## 콘솔(Console)
콘솔은 컴퓨터에서 텍스트 기반의 사용자 인터페이스를 제공하는 환경을 가리킨다. 주로 명령줄 인터페이스(Command Line Interface, CLI)나 터미널에서 사용되며, 사용자는 명령어를 입력하고 프로그램의 출력을 텍스트 형식으로 확인할 수 있다.

여러 운영체제에서 콘솔은 텍스트 기반으로 동작하며, 사용자는 명령어를 입력하여 시스템이나 응용프로그램을 조작할 수 있다. 예를 들어, Windows 운영체제에서는 명령 프롬프트나 PowerShell이 콘솔 환경을 제공하고, Unix/Linux 계열 운영체제에서는 터미널이나 셸이 콘솔과 유사한 역할을 한다.

C#에서의 콘솔은 'System.Console' 클래스를 통해 제어된다. 이 클래스를 사용하여 텍스트를 출력하고나 사용자로부터 텍스트를 입력받을 수 있다. 'Console.WriteLine()'과 'Consoel.ReadLine()'은 이러한 콘솔 환경에서의 입출력을 담당하는 메서드이다.

콘솔은 주로 개발자들이 프로그램을 테스트하거나 디버깅할 때 유용하게 활용되며, 명령줄 기반의 도구나 스크립트 작성에도 사용된다.
---

### Console.Write

Write는 Console의 멤버이며 텍스트 문자열을 프로그램의 콘솔창으로 보낸다. C#에서 문자열을 출력하기 위해서는 큰따옴표로 감싸야 한다. (C#에서 큰따옴표로 감싼 리터럴은 문자열이고, 작은 따옴표로 감싼 리터럴은 문자이다.)

```
Console.Write("Hello, World!");

/* 출력 결과
Hello, World!
*/
```

string 객체를 전달하는 방법은 다음과 같다.

```
string str = "Hello, World!";
Console.Write(str);

/* 출력 결과
Hello, World!
*/
```

Write 메소드에는 이스케이프 시퀀스를 사용할 수 있다.

```
string str = "Hello, World!\n";
Console.Write(str);
Console.Write(str);

/* 출력 결과
Hello, World!
Hello, World!

*/
```

---

### Console.WriteLine

WriteLine은 Write 메서드와 기능은 똑같지만 문자열을 출력시키고 다음 줄로 넘어간다.

```
Console.WriteLine("Hello, World!");
Console.WriteLine("Hello, World!");
Console.WriteLine("Hello, World!");

/* 출력 결과
Hello, World!
Hello, World!
Hello, World!

*/
```

---

### Console.ReadLine

Console.ReadLine은 C#에서 사용자로부터 한 줄의 텍스트를 입력받기 위해 사용되는 메서드이다. 즉, 사용자가 Enter 키를 누를 때 까지의 텍스트를 문자열로 반환한다. 이 메서드를 통해 사용자와 상호작용하며 프로그램의 동작을 유연하게 조절할 수 있다.

```
string name = Console.ReadLine();
Console.Write("My name is ");
Console.WriteLine(name);
```

---

### 문자열 결합

문자열 결합(concatenate)은 + 연산자를 사용한다

```
Console.Write("Hello, " + "World!");

/* 출력 결과
Hello, World!
*/
```

숫자 타입과 문자열을 결합할 수도 있다. 이 경우 숫자 타입이 문자열로 자동 변환된다.

```
int age = 20;
Console.WriteLine("age is " + age);
// Console.WriteLine("age is " + age.ToString()); 과 같음

/* 출력 결과
age is 20
*/
```

---

### String.Format(복합 형식 지정)

String.Format 메서드는 문자열 서식을 사용하여 문자열을 조합하는 데 사용되는 메서드이다. 서식 지정된 문자열을 생성하는 데 도움이 되며, 문자열을 동적으로 조립할 수 있게 해준다.

```
int a = 10;
int b = 20;
int c = 30;
string str = String.Format("{0} + {1} = {2}", a, b, c);
Console.WriteLine(str);

/* 출력 결과
10 + 20 = 30
*/
```

WriteLine에 직접 String.Format처럼 사용할 수도 있다.

```
Console.WriteLine("{0} + {1} = {2}", 10, 20, 30);

/* 출력 결과
10 + 20 = 30
*/
```

---

### 문자열 보간(String interpolation)

문자열 보간은 문자열을 편리하게 형식화하는 방법을 제공한다. 문자열 보간은 '&' 기호를 사용하며, 중괄호 안에 변수나 표현식을 넣어 사용한다.

```
string name = "John";
int age = 30;
string str = $"Name : {name}, Age : {age}";
Console.WriteLine(str);

/* 출력 결과
Name : John, Age : 30
*/
```

또한 문자열 보간은 표현식을 포함할 수 있어 변수 뿐만 아니라 임의의 표현식도 삽입할 수 있다.

```
int x = 10;
int y = 5;
string result = $"{x} + {y} = {x + y}, {x} - {y} = {x-y}";
Console.WriteLine(result);

/* 출력 결과
10 + 5 = 15, 10 - 5 = 5
*/
```
