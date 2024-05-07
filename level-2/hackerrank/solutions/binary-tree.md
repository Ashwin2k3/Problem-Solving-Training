# HackerRank OJ - Binary Tree `20 problems`

## Tree: Preorder Traversal
Problem Link: https://hackerrank.com/challenges/tree-preorder-traversal/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
void preOrder(Node* root) {
    vector<int> res;
    stack<Node*> stk;
    stk.push(root);
    while (not stk.empty()) {
        Node *curr = stk.top();
        stk.pop();
        if (curr->right != NULL)
            stk.push(curr->right);
        if (curr->left != NULL)
            stk.push(curr->left);
        res.push_back(curr->data);
    }
    for (int &i : res)
        cout << i << ' ';
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def preOrder(root):
    res = []
    stk = []
    stk.append(root)
    while stk:
        curr = stk.pop()
        if curr.right != None:
            stk.append(curr.right)
        if curr.left != None:
            stk.append(curr.left)
        res.append(curr.info)
    print(*res)
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Tree: Postorder Traversal
Problem Link: https://hackerrank.com/challenges/tree-postorder-traversal/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
void postOrder(Node* root) {
    vector<int> res;
    stack<Node*> stk;
    stk.push(root);
    while (not stk.empty()) {
        Node *curr = stk.top();
        stk.pop();
        if (curr->left != NULL)
            stk.push(curr->left);
        if (curr->right != NULL)
            stk.push(curr->right);
        res.push_back(curr->data);
    }
    reverse(res.begin(), res.end());
    for (int &i : res)
        cout << i << ' ';
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def postOrder(root):
    res = []
    stk = []
    stk.append(root)
    while stk:
        curr = stk.pop()
        if curr.left != None:
            stk.append(curr.left)
        if curr.right != None:
            stk.append(curr.right)
        res.append(curr.info)
    res = res[::-1]
    print(*res)
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Tree: Inorder Traversal
Problem Link: https://hackerrank.com/challenges/tree-inorder-traversal/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
void inOrder(Node* root) {
    vector<int> res;
    stack<Node*> stk;
    Node *curr = root;
    while (not stk.empty() or curr) {
        if (curr) {
            stk.push(curr);
            curr = curr->left;
        }
        else {
            curr = stk.top();
            stk.pop();
            res.push_back(curr->data);
            curr = curr->right;
        }
    }
    for (int &i : res)
        cout << i << ' ';
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def inOrder(root):
    res = []
    stk = []
    curr = root
    while stk or curr:
        if curr:
            stk.append(curr)
            curr = curr.left
        else:
            curr = stk.pop()
            res.append(curr.info)
            curr = curr.right
    print(*res)
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Tree: Height of a Binary Tree
Problem Link: https://hackerrank.com/challenges/tree-height-of-a-binary-tree/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
int height(Node *root) {
    int res = 0;
    stack<Node*> stk;
    stack<int> height;
    stk.push(root);
    height.push(0);
    while (not stk.empty()) {
        Node *curr = stk.top();
        stk.pop();
        int curr_height = height.top();
        height.pop();
        if (curr->left != NULL) {
            stk.push(curr->left);
            height.push(curr_height+1);
        }
        if (curr->right != NULL) {
            stk.push(curr->right);
            height.push(curr_height+1);
        }
        res = max(res, curr_height);
    }
    return res;
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def height(root):
    res = 0
    stk = []
    height = []
    stk.append(root)
    height.append(0)
    while stk:
        curr = stk.pop()
        curr_height = height.pop()
        if curr.left != None:
            stk.append(curr.left)
            height.append(curr_height+1)
        if curr.right != None:
            stk.append(curr.right)
            height.append(curr_height+1)
        res = max(res, curr_height)
    return res
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Tree : Top View
Problem Link: https://hackerrank.com/challenges/tree-top-view/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
// TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
# TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Tree: Level Order Traversal
Problem Link: https://hackerrank.com/challenges/tree-level-order-traversal/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
void levelOrder(Node* root) {
    vector<int> res;
    queue<Node*> que;
    que.push(root);
    while (not que.empty()) {
        Node *curr = que.front();
        que.pop();
        if (curr->left != NULL)
            que.push(curr->left);
        if (curr->right != NULL)
            que.push(curr->right);
        res.push_back(curr->data);
    }
    for (int &i : res)
        cout << i << ' ';
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def levelOrder(root):
    res = []
    que = []
    que.append(root)
    while que:
        curr = que.pop(0)
        if curr.left:
            que.append(curr.left)
        if curr.right:
            que.append(curr.right)
        res.append(curr.info)
    print(*res)
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Binary Search Tree : Insertion
Problem Link: https://hackerrank.com/challenges/binary-search-tree-insertion/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
Node* insert(Node *root, int data) {
    if (root == NULL)
        return new Node(data);

    Node *curr = root;
    while (true) {
        if (data < curr->data) {
            if (curr->left)
                curr = curr->left;
            else {
                curr->left = new Node(data);
                break;
            }
        }
        else if (data > curr->data) {
            if (curr->right)
                curr = curr->right;
            else {
                curr->right = new Node(data);
                break;
            }
        }
        else
            break;
    }
    return root;
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def insert(self, val):
    if self.root == None:
        self.root = Node(val)
        return
    curr = self.root
    while True:
        if val < curr.info:
            if curr.left:
                curr = curr.left
            else:
                curr.left = Node(val)
                break
        elif val > curr.info:
            if curr.right:
                curr = curr.right
            else:
                curr.right = Node(val)
                break
        else:
            break
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Binary Search Tree : Lowest Common Ancestor
Problem Link: https://hackerrank.com/challenges/binary-search-tree-lowest-common-ancestor/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
Node* lca(Node* root, int v1,int v2) {
    if (root == NULL)
        return NULL;
    if (v1 > v2) {
        int temp = v2;
        v2 = v1;
        v1 = temp;
    }
    while (root->data < v1 or root->data > v2) {
        if (root->data < v1)
            root = root->right;
        else if (root->data > v2)
            root = root->left;
    }
    return root;
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def lca(root, v1, v2):
    if root == None:
        return None
    if v1 > v2:
        v1, v2 = v2, v1
    while root.info < v1 or root.info > v2:
        if root.info < v1:
            root = root.right
        elif root.info > v2:
            root = root.left
    return root
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Tree: Huffman Decoding
Problem Link: https://hackerrank.com/challenges/tree-huffman-decoding/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
void decode_huff(node* root, string s) {
    string decoded_str = "";
    node *curr = root;
    for (char &c : s) {
        if (c == '0' and curr->left)
            curr = curr->left;
        else if (c == '1' and curr->right)
            curr = curr->right;
        if (not curr->left and not curr->right) {
            decoded_str += curr->data;
            curr = root;
        }
    }
    cout << decoded_str;
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def decodeHuff(root, s):
    decoded_str = ''
    curr = root
    for c in s:
        if c == '0' and curr.left:
            curr = curr.left
        elif c == '1' and curr.right:
            curr = curr.right
        if not curr.left and not curr.right:
            decoded_str += curr.data
            curr = root
    print(decoded_str)
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Swap Nodes [Algo]
Problem Link: https://hackerrank.com/challenges/swap-nodes-algo/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
// TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
# TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Is This a Binary Search Tree?
Problem Link: https://hackerrank.com/challenges/is-binary-search-tree/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
bool checkBst(Node* curr, int min, int max) {
    if (curr == NULL)
        return true;

    return min < curr->data and curr->data < max and
           checkBst(curr->left,  min, curr->data) and
           checkBst(curr->right, curr->data, max);
}
bool checkBST(Node* root) {
    return checkBst(root, -2e9, 2e9);
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
def checkBst(curr, min, max):
    if curr == None:
        return True

    return min < curr.data and curr.data < max and \
           checkBst(curr.left,  min, curr.data) and \
           checkBst(curr.right, curr.data, max)

def check_binary_search_tree_(root):
    return checkBst(root, -2e9, 2e9)
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Self Balancing Tree
Problem Link: https://hackerrank.com/challenges/self-balancing-tree/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
struct node {
    int val, ht;
    node *left, *right;

    node(int val=0) {
        this->val = val;
        this->left = NULL;
        this->right = NULL;
        this->ht = 1;
    }
};
int get_height(node* x) {
    if (x == NULL)
        return 0;
    return x->ht;
}
int get_balance(node* x) {
    if (x == NULL)
        return 0;
    return get_height(x->left) - get_height(x->right);
}
node* rightRotate(node* y) {
    node* x = y->left;
    node* T2 = x->right;

    x->right = y;
    y->left = T2;

    y->ht = max(get_height(y->left), get_height(y->right)) + 1;
    x->ht = max(get_height(x->left), get_height(x->right)) + 1;

    return x;
}
node* leftRotate(node* x) {
    node *y = x->right;
    node *T2 = y->left;

    y->left = x;
    x->right = T2;

    x->ht = max(get_height(x->left), get_height(x->right)) + 1;
    y->ht = max(get_height(y->left), get_height(y->right)) + 1;

    return y;
}
node* insert(node* curr, int val) {
    if (curr == NULL)
        return new node(val);
    if (val < curr->val)
        curr->left = insert(curr->left, val);
    else if (val > curr->val)
        curr->right = insert(curr->right, val);
    curr->ht = 1 + max(get_height(curr->left), get_height(curr->right));

    int balance = get_balance(curr);

    if (balance > 1) {
        if (val < curr->left->val)
            return rightRotate(curr);
        else {
            curr->left = leftRotate(curr->left);
            return rightRotate(curr);
        }
    }
    if (balance < -1) {
        if (val > curr->right->val)
            return leftRotate(curr);
        else {
            curr->right = rightRotate(curr->right);
            return leftRotate(curr);
        }
    }
    return curr;
}
void inorder(node* curr) {
    if (curr) {
        inorder(curr->left);
        int bf = get_balance(curr);
        printf("%d(BF=%d) ", curr->val, bf);
        inorder(curr->right);
    }
}
void preorder(node* curr) {
    if (curr) {
        int bf = get_balance(curr);
        printf("%d(BF=%d) ", curr->val, bf);
        preorder(curr->left);
        preorder(curr->right);
    }
}
void postorder(node* curr) {
    if (curr) {
        postorder(curr->left);
        postorder(curr->right);
        int bf = get_balance(curr);
        printf("%d(BF=%d) ", curr->val, bf);
    }
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class node:
    def __init__(self, val=0):
        self.val = val
        self.left = None
        self.right = None
        self.ht = 1

def get_height(x):
    if x == None:
        return 0
    return x.ht

def get_balance(x):
    if x == None:
        return 0
    return get_height(x.left) - get_height(x.right)

def rightRotate(y):
    x = y.left
    T2 = x.right

    x.right = y
    y.left = T2

    y.ht = max(get_height(y.left), get_height(y.right)) + 1
    x.ht = max(get_height(x.left), get_height(x.right)) + 1

    return x

def leftRotate(x):
    y = x.right
    T2 = y.left

    y.left = x
    x.right = T2

    x.ht = max(get_height(x.left), get_height(x.right)) + 1
    y.ht = max(get_height(y.left), get_height(y.right)) + 1

    return y

def insert(curr, val):
    if curr == None:
        return node(val)
    if val < curr.val:
        curr.left = insert(curr.left, val)
    elif val > curr.val:
        curr.right = insert(curr.right, val)
    curr.ht = 1 + max(get_height(curr.left), get_height(curr.right))

    balance = get_balance(curr)

    if balance > 1:
        if val < curr.left.val:
            return rightRotate(curr)
        else:
            curr.left = leftRotate(curr.left)
            return rightRotate(curr)

    if balance < -1:
        if val > curr.right.val:
            return leftRotate(curr)
        else:
            curr.right = rightRotate(curr.right)
            return leftRotate(curr)

    return curr

def inorder(curr):
    if curr:
        inorder(curr.left)
        bf = get_balance(curr)
        print("{}(BF={})".format(curr.val, bf), end=" ")
        inorder(curr.right)

def preorder(curr):
    if curr:
        bf = get_balance(curr)
        print("{}(BF={})".format(curr.val, bf), end=" ")
        preorder(curr.left)
        preorder(curr.right)

def postorder(curr):
    if curr:
        postorder(curr.left)
        postorder(curr.right)
        bf = get_balance(curr)
        print("{}(BF={})".format(curr.val, bf), end=" ")
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## QHEAP1
Problem Link: https://hackerrank.com/challenges/qheap1/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
// TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
# TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Jesse and Cookies
Problem Link: https://hackerrank.com/challenges/jesse-and-cookies/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
int cookies(int k, vector<int> &A) {
    auto comp = [](const int &x, const int &y) { return x > y; };
    priority_queue<int, vector<int>, decltype(comp)> min_heap(comp);
    for (int i : A)
        min_heap.push(i);
    int res = 0;
    while (not min_heap.empty()) {
        int a = min_heap.top();
        min_heap.pop();
        if (a >= k or min_heap.empty()) {
            min_heap.push(a);
            break;
        }
        int b = min_heap.top();
        min_heap.pop();
        min_heap.push(a + 2 * b);
        res ++;
    }
    if (min_heap.top() >= k)
        return res;
    else
        return -1;
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
import queue

def cookies(k, A):
    min_heap = queue.PriorityQueue()
    for i in A:
        min_heap.put(i)
    res = 0
    while not min_heap.empty():
        a = min_heap.get()
        if a >= k or min_heap.empty():
            min_heap.put(a)
            break
        b = min_heap.get()
        min_heap.put(a + 2 * b)
        res += 1
    if min_heap.queue[0] >= k:
        return res
    else:
        return -1
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Components in a graph
Problem Link: https://hackerrank.com/challenges/components-in-graph/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
class disjoint_set {
public:
    class Node {
    public:
        int data, rank;
        Node* parent;
        Node(int data=0) {
            this->data = data;
            this->parent = this;
            this->rank = 0;
        }
    };

    map<int, Node*> items;
    void make_set(int data) {
        if (this->items.find(data) == items.end())
            this->items[data] = new Node(data);
    }
    Node* find_set(int data) {
        if (this->items.find(data) == items.end())
            return NULL;
        Node* node = this->items[data];
        if (node->parent == node)
            return node;
        node->parent = find_set(node->parent->data);
        return node->parent;
    }
    void union_set(int node1, int node2) {
        Node* parent1 = find_set(node1);
        Node* parent2 = find_set(node2);
        if (parent1 and parent2 and parent1 != parent2) {
            if (parent1->rank > parent2->rank)
                parent2->parent = parent1;
            else if (parent1->rank < parent2->rank)
                parent1->parent = parent2;
            else {
                parent1->rank ++;
                parent2->parent = parent1;
            }
        }
    }
};

vector<int> componentsInGraph(vector<vector<int>> gb) {
    int n = size(gb);
    vector<int> res(n+1, 0);
    disjoint_set dj_set;
    int dj_set_max = 0;
    int dj_set_min = n+1;
    for (auto &it : gb) {
        dj_set.make_set(it[0]);
        dj_set.make_set(it[1]);
        dj_set.union_set(it[0], it[1]);
    }
    for (auto &[i, j] : dj_set.items) {
        int x = dj_set.find_set(i)->data;
        res[x] ++;
    }
    for (auto &[i, j] : dj_set.items) {
        int x = dj_set.find_set(i)->data;
        dj_set_max = max(dj_set_max, res[x]);
        if (res[x] > 1)
            dj_set_min = min(dj_set_min, res[x]);
    }
    return {dj_set_min, dj_set_max};
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class disjoint_set:
    class Node:
        def __init__(self, data=0):
            self.data = data
            self.parent = self
            self.rank = 0

    def __init__(self):
        self.items = dict()

    def make_set(self, data):
        if data not in self.items:
            self.items[data] = self.Node(data)

    def find_set(self, data):
        if data not in self.items:
            return None
        node = self.items[data]
        if node.parent == node:
            return node
        node.parent = self.find_set(node.parent.data)
        return node.parent

    def union_set(self, node1, node2):
        parent1 = self.find_set(node1)
        parent2 = self.find_set(node2)
        if parent1 and parent2 and parent1 != parent2:
            if parent1.rank > parent2.rank:
                parent2.parent = parent1
            elif parent1.rank < parent2.rank:
                parent1.parent = parent2
            else:
                parent1.rank += 1
                parent2.parent = parent1

def componentsInGraph(gb):
    n = len(gb)
    res = [0] * (n+1)
    dj_set = disjoint_set()
    dj_set_max = 0
    dj_set_min = n+1
    for a, b in gb:
        dj_set.make_set(a)
        dj_set.make_set(b)
        dj_set.union_set(a, b)
    for i in dj_set.items.keys():
        x = dj_set.find_set(i).data
        res[x] += 1
    for i in dj_set.items.keys():
        x = dj_set.find_set(i).data
        dj_set_max = max(dj_set_max, res[x])
        if res[x] > 1:
            dj_set_min = min(dj_set_min, res[x])
    return [dj_set_min, dj_set_max]
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Contacts
Problem Link: https://hackerrank.com/challenges/contacts/problem

<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/c.png"></img></picture>
<details>
    <summary>C Solution</summary>

```c

```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></picture>
<details>
    <summary>C++ Solution</summary>

```cpp
class TrieNode {
public:
    vector<TrieNode*> child;
    int cnt;
    TrieNode() {
        this->child.assign(26, NULL);
        this->cnt = 0;
    }
};

class Trie {
public:
    TrieNode *root;
    Trie() {
        this->root = new TrieNode();
    }
    void insert(string word) {
        TrieNode *curr = this->root;
        for (char c : word) {
            int i = c - 'a';
            if (curr->child[i] == NULL)
                curr->child[i] = new TrieNode();
            curr = curr->child[i];
            curr->cnt ++;
        }
    }
    int find(string word) {
        TrieNode *curr = this->root;
        int res = 0;
        for (char c : word) {
            int i = c - 'a';
            if (curr->child[i] != NULL) {
                curr = curr->child[i];
                res = curr->cnt;
            }
            else {
                res = 0;
                break;
            }
        }
        return res;
    }
};

vector<int> contacts(vector<vector<string>> queries) {
    Trie t = Trie();
    vector<int> res;
    for (auto &it : queries) {
        string op = it[0], w = it[1];
        if (op == "add")
            t.insert(w);
        else if (op == "find")
            res.push_back(t.find(w));
    }
    return res;
}
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Trie:
    class TrieNode:
        def __init__(self):
            self.child = [None] * 26
            self.cnt = 0

    def __init__(self):
        self.root = self.TrieNode()

    def insert(self, word):
        curr = self.root
        for c in word:
            i = ord(c) - ord('a')
            if curr.child[i] == None:
                curr.child[i] = self.TrieNode()
            curr = curr.child[i]
            curr.cnt += 1

    def find(self, word):
        curr = self.root
        res = 0
        for c in word:
            i = ord(c) - ord('a')
            if curr.child[i] != None:
                curr = curr.child[i]
                res = curr.cnt
            else:
                res = 0
                break
        return res

def contacts(queries):
    t = Trie()
    res = []
    for op, w in queries:
        if op == 'add':
            t.insert(w)
        elif op == 'find':
            res.append(t.find(w))
    return res
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Kindergarten Adventures
Problem Link: https://hackerrank.com/challenges/kindergarten-adventures/problem

<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></a>
<details>
    <summary>C++ Solution</summary>

```cpp
int solve(vector<int> &t) {
    int n = size(t);
    vector<int> arr(n+1, 0);
    int i = 0;
    while (i < n) {
        int r1 = max(0, i+1-t[i]);
        int r2 = min(max(0, n-t[i])+i+1, n);
        arr[0] ++;
        arr[i+1] ++;
        arr[r1] --;
        arr[r2] --;
        i ++;
    }
    for (int i=0; i<n; i++)
        arr[i+1] += arr[i];
    int max_arr = *max_element(arr.begin(), arr.end());
    return find(arr.begin(), arr.end(), max_arr)-arr.begin()+1;
}
```

</details>
<br>
<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></a>
<details>
    <summary>Python Solution</summary>

```python
def solve(t):
    n = len(t)
    arr = [0] * (n + 1)
    i = 0
    while i < n:
        r1 = max(0, i+1-t[i])
        r2 = min(max(0, n-t[i])+i+1, n)
        arr[0] +=  1
        arr[i+1] += 1
        arr[r1] -= 1
        arr[r2] -= 1
        i += 1
    for i in range(n):
        arr[i+1] += arr[i]
    return arr.index(max(arr))+1
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Mr. X and His Shots
Problem Link: https://hackerrank.com/challenges/x-and-his-shots/problem

<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></a>
<details>
    <summary>C++ Solution</summary>

```cpp
// TODO
```

</details>
<br>
<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></a>
<details>
    <summary>Python Solution</summary>

```python
# TODO
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Jim and the Skyscrapers
Problem Link: https://hackerrank.com/challenges/jim-and-the-skyscrapers/problem

<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></a>
<details>
    <summary>C++ Solution</summary>

```cpp
const int N = 3e5+3;
int a[N], b[N];

void printNGE(vector<int> &v) {
    stack<int> stk;
    stk.push(0);
    for (int i=1; i<size(v); i++) {
        while (!stk.empty() and v[stk.top()] <= v[i]) {
            a[stk.top()] = i;
            stk.pop();
        }
        stk.push(i);
    }
    while (!stk.empty()) {
        a[stk.top()] = -1;
        stk.pop();
    }
}
long solve(vector<int> &arr) {
    printNGE(arr);
    long res = 0;
    for (int i=0; i<size(arr); i++) {
        if (arr[i] == arr[a[i]])
            b[a[i]] = b[i] + 1;
    }
    for (int i=0; i<size(arr); i++)
        res += b[i];
    return 2LL * res;
}
```

</details>
<br>
<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></a>
<details>
    <summary>Python Solution</summary>

```python
N = int(3e5+3)
a = [0] * N
b = [0] * N

def printNGE(v):
    stk = []
    stk.append(0)
    for i in range(1, len(v)):
        while stk and v[stk[-1]] <= v[i]:
            a[stk[-1]] = i
            stk.pop()
        stk.append(i)
    while stk:
        a[stk[-1]] = -1
        stk.pop()

def solve(arr):
    printNGE(arr)
    res = 0
    for i in range(len(arr)):
        if arr[i] == arr[a[i]]:
            b[a[i]] = b[i] + 1
    for i in range(len(arr)):
        res += b[i]
    return 2 * res
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>

## Find Maximum Index Product
Problem Link: https://hackerrank.com/challenges/find-maximum-index-product/problem

<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/cpp.png"></img></a>
<details>
    <summary>C++ Solution</summary>

```cpp
vector<int> find_direction(vector<int> &arr, bool direction) {
    stack<int> stk;
    stk.push(1);
    vector<int> res;
    for (int i=1; i<size(arr)-1; i++) {
        while (!stk.empty() and arr[stk.top()-1] <= arr[i])
            stk.pop();
        int temp;
        if (direction)
            temp = (!stk.empty()? stk.top() : 0);
        else
            temp = (!stk.empty()? size(arr) - stk.top() + 1 : 0);
        res.push_back(temp);
        stk.push(i+1);
    }
    return res;
}
long solve(vector<int> &arr) {
    long res = 0LL;
    vector<int> left = find_direction(arr, true);
    reverse(arr.begin(), arr.end());
    vector<int> right = find_direction(arr, false);
    reverse(right.begin(), right.end());
    for (int i=0; i<size(left); i++)
        res = max(1LL * res, 1LL * left[i] * right[i]);
    return res;
}
```

</details>
<br>
<a href="/level-2/hackerrank/data-structures/solutions/advanced-I.md"><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></a>
<details>
    <summary>Python Solution</summary>

```python
def find_direction(arr, direction):
    stk = [1]
    res = []
    for i in range(1, len(arr)-1):
        while stk and arr[stk[-1]-1] <= arr[i]:
            stk.pop()
        if direction:
            temp = stk[-1] if stk else 0
        else:
            temp = len(arr) - stk[-1] + 1 if stk else 0
        res.append(temp)
        stk.append(i+1)
    return res

def solve(arr):
    res = 0
    left = find_direction(arr, True)
    arr = arr[::-1]
    right = find_direction(arr, False)
    right = right[::-1]
    for i in range(len(left)):
        res = max(res, left[i] * right[i])
    return res
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/golang.png"></img></picture>
<details>
    <summary>Go Solution</summary>

```go

```

</details>
<br>
