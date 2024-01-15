## 스택(Stack)

스택은 LIFO(Last In First Out) 원칙에 따라 동작하는 선형 자료구조 입니다. 이는 마지막에 들어온 데이터가 가장 먼저 나가게 됩니다. 이런 특성 때문에 데이터의 삽입과 삭제가 한 쪽 끝에서만 이루어집니다.

### 특징

1. LIFO 원칙 : 스택은 마지막에 들어온 데이터가 가장 먼저 나가게 됩니다. 이는 스택의 가장 상위에 데이터를 추가하고, 가장 상위의 데이터를 제거하는 방식으로 동작하게 됩니다.

2. 한 쪽 끝에서만 동작 : 데이터의 삽입(push)과 삭제(pop)가 스택의 가장 상위(top)에서만 이루어집니다. 이는 스택의 구조를 단순하게 만들면서도 효율적인 동작을 가능하게 합니다.

### 장점

1. 단순한 자료구조 : 스택은 매우 단순한 자료구조로, 구현이 간단하며 데이터의 관리가 용이합니다.

2. LIFO 원칙 : 이 원칙에 따라 동작하는 특성 때문에, 깊이 우선 탐색(DFS), 실행 취소(undo), 후위 표기법 등의 알고리즘에 활용됩니다.

### 단점

1. 데이터 접근의 제한 : 스택은 가장 상위의 데이터에만 접근할 수 있습니다. 따라서, 스택 내부의 데이터를 탐색하거나 접근하는 것이 불가능하므로 사용에 제한이 있습니다.

2. 오버플로우 : 스택의 크기가 고정되어 있을 경우, 스택이 가득 차면 더 이상 데이터를 추가할 수 없으므로 오버플로우가 발생할 수 있습니다.

### 사용 예시

스택은 실행 취소(undo), 뒤로가기(back), 깊이 우선 탐색(DFS), 후위 표기법(postfix notation), 메모리 관리 등의 다양한 알고리즘에서 활용됩니다.

---

## Push

스택에 데이터를 삽입하는 작업이다. Push는 다음 단계를 거쳐 진행됩니다.

1. 스택이 가득 찼는지 확인합니다.
2. 스택이 가득 찼으면 오류를 발생하고 종료합니다.
3. 스택이 가득 차지 않았으면 Top을 증가시킵니다.
4. Top이 가리키는 위치에 데이터를 삽입합니다.

## Pop

스택의 데이터를 제거하는 작업이다. Pop은 다음 단계를 거쳐 진행됩니다.

1. 스택이 비어있는지 확인합니다.
2. 스택이 비어있으면 오류를 발생하고 종료합니다.
3. 스택이 비어있지 않으면 Top이 가리키는 데이터를 제거합니다.
4. Top을 감소시킵니다.

---

```
using System;

class Program
{
    public static void Main(string[] args)
    {
        // 스택 생성
        Stack<string> stack = new Stack<string>();

        // 값 추가
        stack.Push("value 1");
        stack.Push("value 2");
        stack.Push("value 3");

        // 값 출력
        foreach(string value in stack)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");

        // 값 제거
        string popValue = stack.Pop();
        Console.WriteLine($"Pop으로 제거된 값 : {popValue}");

        // 스택의 상단 값 확인
        string peekValue = stack.Peek();
        Console.WriteLine($"Peek으로 확인된 상단의 값 : {peekValue}");

        // 스택의 크기
        Console.WriteLine($"스택의 크기 : {stack.Count}");

        // 스택 내부의 특정 값 존재 여부
        Console.WriteLine($"value 1 값 존재 여부 : {stack.Contains("value 1")}");
    }
}
```

<br>
출력 결과
<br>
<img src=https://velog.velcdn.com/images/dbsdbds4532/post/63346293-9d22-4d6e-9962-cfdd8a5bdf25/image.png>
