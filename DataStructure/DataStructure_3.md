---
## 배열(Array)
배열은 같은 타입의 데이터 요소들을 연속적인 메모리 공간에 저장하는 가장 기본적인 자료구조입니다.

### 특징
1. 동일한 데이터 타입 : 배열은 동일한 데이터 타입의 요소들로 이루어져 있습니다.

2. 연속적인 메모리 공간 : 배열의 모든 요소들은 연속적인 메모리 공간에 저장됩니다. 이로 인해 배열은 인덱스를 통해 각 요소에 빠르게 접근할 수 있습니다.

### 장점
1. 빠른 접근 속도 : 배열은 인덱스를 통해 각 요소에 O(1)의 시간 복잡도로 접근할 수 있습니다.

2. 데이터의 순서 유지 : 배열은 데이터의 순서를 유지합니다. 즉, 데이터가 배열에 추가된 순서대로 저장되므로, 순서가 중요한 경우 유용하게 사용할 수 있습니다.

### 단점
1. 크기 변경의 어려움 : 배열은 크기를 변경하는 것이 일반적으로 어렵습니다. 새로운 요소를 추가하거나 기존 요소를 삭제할 때, 새로운 배열을 생성하고 복사해야 하는 불편함이 있습니다.

2. 메모리 낭비 : 배열의 크기는 고정되어 있기 때문에, 모든 공간을 사용하지 않아도 그 만큼의 메모리는 차지하게 됩니다. 이로 인해 메모리 낭비가 발생할 수 있습니다.

### 사용 예시
배열은 다양한 프로그래밍 상황에서 사용됩니다. 예를 들어, 데이터의 집합을 저장하고 순서대로 접근해야 하는 경우, 배열은 매우 효과적인 자료구조입니다. 또한, 다차원 배열을 사용하면 행렬이나 그래프 등의 복잡한 데이터 구조를 표현할 수 있습니다.
배열은 그 구조가 간단하고 사용하기 쉬워서, 프로그래밍을 처음 배우는 사람들이나 단순한 데이터 관리에 주로 사용됩니다. 하지만 데이터의 동적인 추가와 삭제가 빈번하게 일어나는 경우에는 다른 자료구조를 사용하는 것이 더 효율적일 수 있습니다.

---

```
using System;

class Program
{
    static void Main()
    {
        // 배열 생성
        int[] array = new int[5];

        // 배열에 값 할당
        array[0] = 10;
        array[1] = 10;
        array[2] = 10;
        array[3] = 10;
        array[4] = 10;

        // 배열의 값 출력
        for(int i = 0; i < array.Length; i++)
        {
            Console.WriteLine($"Element at index {i} : {array[i]}");
        }

        // 2차원 배열 생성과 동시에 초기화
        int[,] matrix = new int[3, 2]{{10, 20}, {30, 40}, {50, 60}};

        // 배열의 값 출력
        for(int i = 0; i < matrix.GetLength(0); i++)
        {
            for(int j = 0; j < matrix.GetLength(1); j++)
            {
                Console.WriteLine($"Element at index [{i},{j}]: {matrix[i,j]}");
            }
        }
    }
}
```

<br>
출력 결과
<br>
<img src="https://velog.velcdn.com/images/dbsdbds4532/post/a584fc36-12ee-4b03-8bd8-3b6ed979bef9/image.png" width="300px" align="left">