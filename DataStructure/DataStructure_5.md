---
## 순차 리스트(Sequential List)
순차 리스트는 데이터를 연속적인 메모리 공간에 순차적으로 저장하는 가장 기본적인 자료구조입니다. 이는 배열과 매우 유사한 형태를 가지며, 인덱스를 통해 각 요소에 빠르게 접근할 수 있습니다.

### 특징
1. 순차적인 데이터 저장 : 데이터는 메모리 공간에 순차적으로 저장됩니다. 이는 데이터의 순서를 유지하면서, 인덱스를 통한 빠른 접근을 가능하게 합니다.

2. 고정된 크기 : 순차 리스트는 일반적으로 크기가 고정되어 있습니다. 이는 데이터의 추가나 삭제가 비교적 불편하다는 단점을 가집니다. 하지만 동적 배열이나 리스트를 통해 이 문제를 해결할 수 있습니다.

### 장점
1. 빠른 접근 속도 : 인덱스를 통해 각 요소에 빠르게 접근할 수 있습니다. 이는 배열이나 리스트에 비해 빠른 검색 속도를 가집니다.

2. 메모리 효율 : 데이터가 순차적으로 저장되므로, 메모리 공간을 효율적으로 활용할 수 있습니다.

### 단점
1. 데이터 추가/삭제의 어려움 : 데이터를 추가하거나 삭제하는 경우, 해당 위치 이후의 모든 데이터를 이동해야 하므로 비효율적입니다. 이 문제는 동적 배열이나 리스트를 통해 해결할 수 있습니다.

2. 크기 변경의 어려움 : 일반적으로 순차 리스트의 크기는 고정되어 있으므로, 크기를 변경하는 것이 어렵습니다. 이는 데이터의 동적인 추가나 삭제가 빈번하게 일어나는 경우, 사용하기 어렵다는 단점을 가집니다.

### 사용 예시
순차 리스트는 데이터의 순서가 중요하고, 빠른 검색이 필요한 경우에 주로 사용됩니다. 예를 들어, 데이터베이스의 레코드 저장이나, 파일 시스템의 블록 저장 등에 사용될 수 있습니다.

---

```
using System;
using System.Collections;

class Program
{
    static void Main()
    {
        // 순차 리스트 생성
        ArrayList arrayList = new ArrayList();

        // 값 추가
        arrayList.Add("value 1");
        arrayList.Add("value 2");
        arrayList.Add("value 3");

        // 값 출력
        foreach (string value in arrayList)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");


        // 값 제거
        arrayList.Remove("value 1");

        // 특정 위치에 값 추가
        arrayList.Insert(2, "value 4");

        // 값 출력
        Console.WriteLine("arrayList의 value 1 값 제거, value 4 값 추가 결과");
        foreach (string value in arrayList)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");


        // 특정 위치의 값 제거
        arrayList.RemoveAt(2);

        // 값 출력
        Console.WriteLine("2번 인덱스 값 제거 결과");
        foreach (string value in arrayList)
        {
            Console.WriteLine(value);
        }
        Console.WriteLine("----------");

        // ArrayList 크기
        Console.WriteLine("arrayList의 크기 : " + arrayList.Count);

        // ArrayList 내부의 특정 값 존재 여부
        Console.WriteLine("value 2 값 존재 여부 : " + arrayList.Contains("value 2"));
    }
}
```

<br>
출력 결과
<br>
<img src =https://velog.velcdn.com/images/dbsdbds4532/post/d8838483-5022-4d7f-80d2-74197552b5a0/image.png>
