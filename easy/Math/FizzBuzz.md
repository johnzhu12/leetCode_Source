# [FizzBuzz](https://leetcode-cn.com/explore/interview/card/top-interview-questions-easy/25/math/60/)

![fizzBuzz](./imgs/fizzBuzz.png)

## 思路

### 1.暴力解决

循环判断

```js
var fizzBuzz = function (n) {
    var ans = []
    for (var i = 1; i <= n; i++) {
        if (i % 3 != 0 && i % 5 != 0) { //不是3或者5的倍数
            ans.push(`${i}`)    //注意这里，一开始没注意是字符串
        } else if (i % 3 == 0 && i % 5 == 0) {//同时是3或者5的倍数
            ans.push('FizzBuzz')
        } else if (i % 3 == 0 && i % 5 != 0) {//只是3的倍数
            ans.push('Fizz')
        } else {
            ans.push('Buzz')
        }
    }
    return ans;
};

```

