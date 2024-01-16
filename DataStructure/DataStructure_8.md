## 큐(Queue)

큐는 FIFO(First In First Out) 원칙에 따라 동작하는 선형 자료구조입니다. 이는 첫 번째로 들어온 데이터가 가장 먼저 나가게 되는 구조를 말합니다. 큐의 경우, 데이터의 삽입이 한 쪽 끝에서 이루어지고, 데이터의 삭제가 반대쪽 끝에서 이루어집니다.

### 특징

1. FIFO 원칙 : 첫 번째로 들어온 데이터가 가장 먼저 나가게 됩니다. 이는 큐의 가장 마지막(rear)에 데이터를 추가하고, 가장 처음(front)의 데이터를 제거하는 방식으로 동작합니다.

2. 두 쪽 끝에서 동작 : 데이터 삽입(enqueue)과 삭제(dequeue)가 큐의 두 끝에서 각각 이루어집니다. 이는 큐의 구조를 단순하게 만들면서도 효율적인 동작을 가능하게 합니다.

### 장점

1. 단순한 자료구조 : 큐는 매우 단순한 자료구조로, 구현이 간단하며 데이터의 관리가 용이합니다.

2. FIFO 원칙 : 이 원칙에 따라 동작하는 특성 때문에, 너비 우선 탐색(BFS), 버퍼, 캐시 등의 알고리즘에 활용됩니다.

### 단점

1. 데이터 접근의 제한 : 큐는 가장 처음의 데이터에만 접근할 수 있습니다. 따라서, 큐 내부의 데이터를 탐색하거나 접근하는 것이 불가능하므로 사용에 제한이 있습니다.

2. 언더플로우 : 큐가 비어있을 때 데이터를 삭제하려고 하면 언더플로우가 발생할 수 있습니다.

### 사용 예시

큐는 일정한 순서를 유지해야 하는 작업에 유용하며, 너비 우선 탐색(BFS), 버퍼, 캐시, 프린터의 인쇄 대기열 등 다양한 알고리즘과 시스템에서 활용됩니다.

---

```
using System;

class Program
{
    public static void Main(string[] args)
    {
        // 큐 생성
        Queue<string> queue = new Queue<string>();

        // 값 추가
        queue.Enqueue("value 1");
        queue.Enqueue("value 2");
        queue.Enqueue("value 3");

        // 값 출력
        foreach(string value in queue)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");

        // 값 제거
        string dequeueValue = queue.Dequeue();
        Console.WriteLine($"Dequeue로 제거된 값 : {dequeueValue}");

        // 큐의 첫번째 값 확인
        string peekValue = queue.Peek();
        Console.WriteLine($"Peek으로 확인된 첫번째 값 : {peekValue}");

        // 큐의 크기
        Console.WriteLine($"큐의 크기 : {queue.Count}");

        // 큐 내부의 특정 값 존재 여부
        Console.WriteLine($"value 3 값 존재 여부 : {queue.Contains("value 3")}");
    }
}
```

<br>
출력 결과
<br>
<img src=https://velog.velcdn.com/images/dbsdbds4532/post/0c29cc6c-4375-4482-b7be-cff1d148adc1/image.png>
