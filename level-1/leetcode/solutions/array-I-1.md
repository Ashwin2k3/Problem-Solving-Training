# LeetCode OJ - Array I `15 problems`

## Running Sum of 1d Array
Problem Link: https://leetcode.com/problems/running-sum-of-1d-array/

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
class Solution {
public:
    vector<int> runningSum(vector<int> &nums) {
        vector<int> res(size(nums));
        int curr_sum = 0;
        for (int i = 0; i < size(nums); i++) {
            curr_sum += nums[i];
            res[i] = curr_sum;
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        res = [0] * len(nums)
        curr_sum = 0
        for i in range(len(nums)):
            curr_sum += nums[i]
            res[i] = curr_sum
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

## Kids With the Greatest Number of Candies
Problem Link: https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/

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
class Solution {
public:
    vector<bool> kidsWithCandies(vector<int> &candies, int extraCandies) {
        int max_candies = *max_element(candies.begin(), candies.end());
        vector<bool> res(size(candies), false);
        for (int i = 0; i < size(candies); i++) {
            if (candies[i] + extraCandies >= max_candies)
                res[i] = true;
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def kidsWithCandies(self, candies: List[int], extraCandies: int) -> List[bool]:
        max_candies = max(candies)
        res = [False] * len(candies)
        for i in range(len(candies)):
            if candies[i] + extraCandies >= max_candies:
                res[i] = True
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

## Richest Customer Wealth
Problem Link: https://leetcode.com/problems/richest-customer-wealth/

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
class Solution {
public:
    int maximumWealth(vector<vector<int>> &accounts) {
        int res = 0;    
        for (const auto &account : accounts) {
            int wealth = accumulate(account.begin(), account.end(), 0);        
            res = max(res, wealth);
        }    
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def maximumWealth(self, accounts: List[List[int]]) -> int:
        res = 0
        for account in accounts:
            wealth = sum(account)
            res = max(res, wealth)
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

## Shuffle the Array
Problem Link: https://leetcode.com/problems/shuffle-the-array/

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
class Solution {
public:
    vector<int> shuffle(vector<int> &nums, int n) {
        vector<int> res(2*n);        
        for (int i = 0; i < n; i++) {
            res[2*i] = nums[i];
            res[2*i+1] = nums[i+n];
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def shuffle(self, nums: List[int], n: int) -> List[int]:
        res = [0] * (2*n)
        for i in range(n):
            res[2*i] = nums[i]
            res[2*i+1] = nums[i + n]
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

## Decompress Run-Length Encoded List
Problem Link: https://leetcode.com/problems/decompress-run-length-encoded-list/

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
class Solution {
public:
    vector<int> decompressRLElist(vector<int> &nums) {
        vector<int> res;
        for (int i = 0; i < size(nums); i+=2) {
            for (int j = 0; j < nums[i]; j++)
                res.push_back(nums[i+1]);
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def decompressRLElist(self, nums: List[int]) -> List[int]:
        res = []
        for i in range(0, len(nums), 2):
            for j in range(nums[i]):
                res.append(nums[i+1])
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

## Create Target Array in the Given Order
Problem Link: https://leetcode.com/problems/create-target-array-in-the-given-order/

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
class Solution {
public:
    vector<int> createTargetArray(vector<int> &nums, vector<int> &index) {
        vector<int> res;
        for (int i = 0; i < size(nums); i++)
            res.insert(res.begin()+index[i], nums[i]);
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def createTargetArray(self, nums: List[int], index: List[int]) -> List[int]:
        res = []
        for i in range(len(nums)):
            res.insert(index[i], nums[i])
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

## Count Items Matching a Rule
Problem Link: https://leetcode.com/problems/count-items-matching-a-rule/

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
class Solution {
public:
    int countMatches(vector<vector<string>> &items, string ruleKey, string ruleValue) {
        int count = 0;
        int index = (ruleKey == "type"? 0 : ruleKey == "color"? 1 : 2);
        for (const auto &item : items) {
            if (item[index] == ruleValue)
                count ++;
        }
        return count;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def countMatches(self, items: List[List[str]], ruleKey: str, ruleValue: str) -> int:
        count = 0
        index = 0 if ruleKey == "type" else 1 if ruleKey == "color" else 2
        for item in items:
            if item[index] == ruleValue:
                count += 1
        return count
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

## XOR Operation in an Array
Problem Link: https://leetcode.com/problems/xor-operation-in-an-array/

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
class Solution {
public:
    int xorOperation(int n, int start) {
        int res = start;
        for (int i = 1; i < n; i++)
            res ^= (start + 2*i);
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def xorOperation(self, n: int, start: int) -> int:
        res = start
        for i in range(1, n):
            res ^= (start + 2*i)
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

## Design an Ordered Stream
Problem Link: https://leetcode.com/problems/design-an-ordered-stream/

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
class OrderedStream {
private:
    vector<string> stream;
    int ptr;
    
public:
    OrderedStream(int n) {
        stream.resize(n+1);
        ptr = 1;
    }
    
    vector<string> insert(int idKey, string value) {
        stream[idKey] = value;
        vector<string> res;
        while (ptr < size(stream) and !stream[ptr].empty()) {
            res.push_back(stream[ptr]);
            ptr ++;
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class OrderedStream:
    def __init__(self, n: int):
        self.stream = [None] * (n+1)
        self.ptr = 1

    def insert(self, idKey: int, value: str) -> List[str]:
        self.stream[idKey] = value
        res = []
        while self.ptr < len(self.stream) and self.stream[self.ptr]:
            res.append(self.stream[self.ptr])
            self.ptr += 1
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

## Sum of All Odd Length Subarrays
Problem Link: https://leetcode.com/problems/sum-of-all-odd-length-subarrays/

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
class Solution {
public:
    int sumOddLengthSubarrays(vector<int> &arr) {
        int n = size(arr);
        int res = 0;
        for (int i = 0; i < n; i++) {
            int left_cnt = i+1;
            int right_cnt = n-i;
            int total_cnt = left_cnt * right_cnt;
            int odd_cnt = total_cnt/2 + (total_cnt%2);
            res += odd_cnt * arr[i];
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def sumOddLengthSubarrays(self, arr: List[int]) -> int:
        n = len(arr)
        res = 0
        for i in range(n):
            left_cnt = i + 1
            right_cnt = n - i
            total_cnt = left_cnt * right_cnt
            odd_cnt = total_cnt // 2 + (total_cnt % 2)
            res += odd_cnt * arr[i]
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

## Count Good Triplets
Problem Link: https://leetcode.com/problems/count-good-triplets/

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
class Solution {
public:
    int countGoodTriplets(vector<int> &arr, int a, int b, int c) {
        int cnt = 0;
        int n = size(arr);
        for (int i = 0; i < n-2; i++) {
            for (int j = i+1; j < n-1; j++) {
                for (int k = j+1; k < n; k++) {
                    if (abs(arr[i] - arr[j]) <= a and 
                        abs(arr[j] - arr[k]) <= b and 
                        abs(arr[i] - arr[k]) <= c) {
                        cnt ++;
                    }
                }
            }
        }
        return cnt;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def countGoodTriplets(self, arr: List[int], a: int, b: int, c: int) -> int:
        cnt = 0
        n = len(arr)
        for i in range(n-2):
            for j in range(i+1, n-1):
                if abs(arr[i] - arr[j]) <= a:
                    for k in range(j+1, n):
                        if abs(arr[j] - arr[k]) <= b and \
                           abs(arr[i] - arr[k]) <= c:
                            cnt += 1
        return cnt
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

## Find the Highest Altitude
Problem Link: https://leetcode.com/problems/find-the-highest-altitude/

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
class Solution {
public:
    int largestAltitude(vector<int> &gain) {
        int curr_sum = 0;
        int res = 0;
        for (const int &i : gain) {
            curr_sum += i;
            res = max(res, curr_sum);
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def largestAltitude(self, gain: List[int]) -> int:
        curr_sum = 0
        res = 0
        for i in gain:
            curr_sum += i
            res = max(res, curr_sum)
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

## Minimum Time Visiting All Points
Problem Link: https://leetcode.com/problems/minimum-time-visiting-all-points/

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
class Solution {
public:
    int minTimeToVisitAllPoints(vector<vector<int>> &points) {
        int res = 0;
        int n = size(points);
        for (int i = 1; i < n; i++) {
            int diff_x = abs(points[i][0] - points[i-1][0]);
            int diff_y = abs(points[i][1] - points[i-1][1]);
            res += std::max(diff_x, diff_y);
        }
        return res;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def minTimeToVisitAllPoints(self, points: List[List[int]]) -> int:
        res = 0
        n = len(points)
        for i in range(1, n):
            diff_x = abs(points[i][0] - points[i-1][0])
            diff_y = abs(points[i][1] - points[i-1][1])
            res += max(diff_x, diff_y)
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

## Flipping an Image
Problem Link: https://leetcode.com/problems/flipping-an-image/

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
class Solution {
public:
    vector<vector<int>> flipAndInvertImage(vector<vector<int>> &image) {
        int n = size(image);
        for (int i = 0; i < n; i++) {
            int left = 0, right = n - 1;
            while (left <= right) {
                image[i][left] = 1 - image[i][left];
                if (left != right) {
                    image[i][right] = 1 - image[i][right];
                    swap(image[i][left], image[i][right]);
                }
                left ++;
                right --;
            }
        }
        return image;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def flipAndInvertImage(self, image: List[List[int]]) -> List[List[int]]:
        n = len(image)
        for i in range(n):
            left = 0
            right = n - 1
            while left <= right:
                image[i][left] = 1 - image[i][left]
                if left != right:
                    image[i][right] = 1 - image[i][right]
                    image[i][left], image[i][right] = image[i][right], image[i][left]
                left += 1
                right -= 1
        return image
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

## Cells with Odd Values in a Matrix
Problem Link: https://leetcode.com/problems/cells-with-odd-values-in-a-matrix/

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
class Solution {
public:
    int oddCells(int n, int m, vector<vector<int>> &indices) {
        vector<vector<int>> res(n, vector<int>(m, 0));
        for (const auto &index : indices) {
            int row = index[0];
            int col = index[1];
            for (int j = 0; j < m; j++)
                res[row][j] ++;
            for (int i = 0; i < n; i++)
                res[i][col] ++;
        }
        int cnt = 0;
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                if (res[i][j] % 2 != 0)
                    cnt ++;
            }
        }
        return cnt;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def oddCells(self, n: int, m: int, indices: List[List[int]]) -> int:
        res = [[0] * m for _ in range(n)]
        for index in indices:
            row = index[0]
            col = index[1]
            for j in range(m):
                res[row][j] += 1
            for i in range(n):
                res[i][col] += 1
        cnt = 0
        for i in range(n):
            for j in range(m):
                if res[i][j] % 2 != 0:
                    cnt += 1
        return cnt
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

## Find Numbers with Even Number of Digits
Problem Link: https://leetcode.com/problems/find-numbers-with-even-number-of-digits/

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
class Solution {
public:
    int findNumbers(vector<int> &nums) {
        int cnt = 0;
        for (int &num : nums) {
            int digits = 0;
            while (num > 0) {
                num /= 10;
                digits ++;
            }
            if (digits % 2 == 0)
                cnt ++;
        }
        return cnt;
    }
};
```

</details>
<br>
<picture><img align="right" width="50" src="https://github.com/cs-MohamedAyman/cs-MohamedAyman/blob/master/logos/python.png"></img></picture>
<details>
    <summary>Python Solution</summary>

```python
class Solution:
    def findNumbers(self, nums: List[int]) -> int:
        cnt = 0
        for num in nums:
            digits = 0
            while num > 0:
                num //= 10
                digits += 1
            if digits % 2 == 0:
                cnt += 1
        return cnt
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
