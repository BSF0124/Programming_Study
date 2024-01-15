---
## 연결 리스트(Linked List)
연결 리스트는 각 노드가 데이터와 포인터를 가지고 한 줄로 연결되어 있는 방식으로 데이터를 저장하는 자료구조입니다. 이 포인터는 다음 노드와의 연결을 담당하며, 이를 통해 데이터가 비선형적으로 저장되는 것을 가능하게 합니다.

### 특징
1. 동적 메모리 할당 : 연결 리스트는 데이터의 삽입과 삭제가 용이하도록 동적으로 메모리를 할당하여 사용합니다. 따라서 크기가 동적으로 변하는 자료구조로 유연한 데이터 관리가 가능합니다.

2. 노드 간 연결 : 각 노드는 다음 노드를 가리키는 포인터(주소)를 가지고 있어, 노드들이 연결되어 순차적으로 데이터를 관리합니다.

### 장점
1. 데이터 추가/삭제의 용이성 : 연결 리스트의 경우, 데이터를 추가하거나 삭제하는 것이 간단합니다. 즉, 데이터를 추가하거나 삭제할 때 해당 위치의 포인터만 변경하면 되므로, 이러한 작업이 비교적 간단합니다.

2. 동적 메모리 할당 : 연결 리스트는 동적으로 메모리를 할당하여 사용하기 때문에, 데이터의 크기가 동적으로 변하는 상황에서 유용합니다.

### 단점
1. 접근 속도 : 연결 리스트는 인덱스를 통한 접근이 아닌, 노드의 연결을 따라 접근해야 하므로 접근 속도가 느립니다.

2. 임의 접근 어려움 : 연결 리스트는 노드들이 포인터로 연결되어 있기 때문에, 임의의 위치에 있는 데이터에 접근하기 위해서는 처음부터 순차적으로 탐색해야 합니다.

3. 추가적인 메모리 공간 사용 : 각 노드가 데이터와 포인터를 가지고 있기 때문에, 순차 리스트에 비해 추가적인 메모리 공간이 필요합니다.

### 종류
1. 단일 연결 리스트(Singly Linked List) : 각 노드가 다음 노드를 가리키는 포인터만을 가지고 있는 연결 리스트입니다.

2. 이중 연결 리스트(Doubly Linked List) : 각 노드가 이전 노드와 다음 노드를 가리키는 포인터를 모두 가지고 있는 연결 리스트입니다. 이를 통해 노드의 앞뒤로 이동이 용이해집니다.

3. 원형 연결 리스트(Circular Linked List) : 마지막 노드가 첫 번째 노드를 가리키는 원형 형태의 연결 리스트입니다. 순차적으로 데이터를 관리하면서 마지막 노드와 첫 번째 노드를 연결하여 반복적인 접근이 가능합니다.

### 사용 예시
연결 리스트는 데이터의 추가나 삭제가 빈번하게 발생하고, 데이터의 크기가 동적으로 변화하는 경우에 주로 사용됩니다. 예를 들어, 메모리 관리, 스택, 큐, 그래프 등의 구현에 사용될 수 있습니다.

---

```
using System;

class Program
{
    public static void Main(string[] args)
    {
        // 연결 리스트 생성
        LinkedList<string> linkedList = new LinkedList<string>();

        // 값 추가
        linkedList.AddLast("value 1");
        linkedList.AddLast("value 2");
        linkedList.AddLast("value 3");

        // 값 출력
        foreach(string value in linkedList)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");

        // 값 제거
        linkedList.Remove("value 1");

        // 특정 위치의 값 추가
        linkedList.AddAfter(linkedList.Find("value 2"), "value 4");

        // 값 출력
        foreach (string value in linkedList)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");

        // LinkedList 크기
        Console.WriteLine($"linkedList의 크기 : {linkedList.Count}");

        // LinkedList 내부의 특정 값 존재 여부
        Console.WriteLine($"value 4 값 존재 여부 : {linkedList.Contains("value 4")}");
    }
}
```

<br> 
출력결과
<br>
<img src="https://velog.velcdn.com/images/dbsdbds4532/post/753c5da3-753d-4491-b939-07cb1a2abded/image.png">
