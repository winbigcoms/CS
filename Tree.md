# Tree

## 트리란

- 그래프의 일종으로 여러 노드가 한 노드를 가리킬수 있는 구조
- 회로 없이 두 노드를 잇는 길이 하나 뿐인 그래프

## 구조

루트 : 부모없는 최상단의 노드

노드 : 트리 구조의 자료 값을 갖고 있는 요소

에지 : 노드 간의 연결선

부모 : 연결된 두 노드 중 상위에 있는 노드

자식 : 연결된 두 노드 중 하위에 있는 노드

경로 : 두 노드를 연결하는 엣지들

잎새 노드 : 자식이 없는 노드

내부 노드 : 잎새 노드를 제외한 모든 노드

레벨, 깊이 : 루트 노드로 부터의 경로 길이

높이 : 트리에서 가장 큰 레벨 값

## 특징

- 하나의 노드에서 다른 노드로 이동하는 길은 유일
- 모든 노드가 열결됨
- 엣지의 수는 노드의 수 - 1 이다.

## 구현

- 이진트리

```
class Node {
    constructor(value, left, right) {
        this.value = value;
        this.left = left;
        this.right = right;
    }
}

class BinaryTree {
    constructor(array) {
        const nodeArray = array.map(el => new Node(el));

        for (let i = 0; i < nodeArray.length; i++) {
            const leftInd = i * 2 + 1;
            const rightInd = i * 2 + 2;
            if (leftInd < nodeArray.length) {
                nodeArray[i].left = nodeArray[leftInd];
            }
            if (rightInd < nodeArray.length) {
                nodeArray[i].right = nodeArray[rightInd];
            }
        }

        this.root = nodeArray[0];
    }

    preorder() {

    }

    inorder() {

    }

    postorder() {

    }

    bfs(value) {

        return false;
    }

    dfs(value) {

        return false;
    }
}
```

