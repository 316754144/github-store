# JavaScript 测试题

## 1

> 描述

计算并返回给定数组 arr 中所有元素的总和.

> 输入

`[ 1, 2, 3, 4 ]`

> 输出

`10`

> 代码

```javascript
const arr = [1, 2, 3, 4]

const sum = (arr) => {
  let sum = 0
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i]
  }
  return sum
}

console.log(sum(arr))
```

## 2

> 描述

移除数组 arr 中的所有值与 item 相等的元素, 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4, 2]` `2`

> 输出

`[1, 3, 4]`

> 代码

```javascript
const arr = [1, 2, 3, 4, 2]
const item = 2

const remove = (arr, item) => {
  const array = []
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] !== item) {
      array.push(arr[i])
    }
  }
  return array
}

console.log(remove(arr, item))
```

## 3

> 描述

移除数组 arr 中的所有值与 item 相等的元素, 直接在给定的 arr 数组上进行操作, 并将结果数组返回.

> 输入

`[1, 2, 2, 3, 4, 2, 2]` `2`

> 输出

`[1, 3, 4]`

> 代码

```javascript
const arr = [1, 2, 2, 3, 4, 2, 2]
const item = 2

const removeWithoutCopy = (arr, item) => {
  let count = 0
  for (let i = 0; i < arr.length - count; i++) {
    if (arr[i] === item) {
      arr.splice(i, 1)
      count++
      i--
    }
  }
}

removeWithoutCopy(arr, item)

console.log(arr)
```

## 4

> 描述

在数组 arr 末尾添加元素 item, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]` `10`

> 输出

`[1, 2, 3, 4, 10]`

> 代码

```javascript
const arr = [1, 2, 3, 4]
const item = 10

const append = (arr, item) => {
  const array = []
  for (let i = 0; i < arr.length; i++) {
    array.push(arr[i])
  }
  array.push(item)
  return array
}

console.log(append(arr, item))
```

## 5

> 描述

删除数组 arr 最后一个元素, 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]`

> 输出

`[1, 2, 3]`

> 代码

```javascript
const arr = [1, 2, 3, 4]

const truncate = (arr) => {
  const array = []
  for (let i = 0; i < arr.length - 1; i++) {
    array.push(arr[i])
  }
  return array
}

console.log(truncate(arr))
```

## 6

> 描述

在数组 arr 开头添加元素 item. 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]` `10`

> 输出

`[10, 1, 2, 3, 4]`

> 代码

```javascript
const arr = [1, 2, 3, 4]
const item = 10

const prepend = (arr, item) => {
  const array = []
  array.push(item)
  for (let i = 0; i < arr.length; i++) {
    array.push(arr[i])
  }
  return array
}

console.log(prepend(arr, item))
```

## 7

> 描述

删除数组 arr 第一个元素, 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]`

> 输出

`[2, 3, 4]`

> 代码

```javascript
const arr = [1, 2, 3, 4]

const cuttail = (arr) => {
  const array = []
  for (let i = 1; i < arr.length; i++) {
    array.push(arr[i])
  }
  return array
}

console.log(cuttail(arr))
```

## 8

> 描述

合并数组 arr1 和数组 arr2, 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]` `['a', 'b', 'c', 1]`

> 输出

`[1, 2, 3, 4, 'a', 'b', 'c', 1]`

> 代码

```javascript
const arr1 = [1, 2, 3, 4]
const arr2 = ['a', 'b', 'c', 1]

const concat = (arr1, arr2) => {
  const array = []
  for (let i = 0; i < arr1.length; i++) {
    array.push(arr1[i])
  }
  for (let i = 0; i < arr2.length; i++) {
    array.push(arr2[i])
  }
  return array
}

console.log(concat(arr1, arr2))
```

## 9

> 描述

在数组 arr 的 index 处添加元素 item, 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]` `'z'` `2`

> 输出

`[1, 2, 'z', 3, 4]`

> 代码

```javascript
const arr = [1, 2, 3, 4]
const item = 'z'
const index = 2

const insert = (arr, item, index) => {
  const array = []
  for (let i = 0; i < index; i++) {
    array.push(arr[i])
  }
  array.push(item)
  for (let i = index; i < arr.length; i++) {
    array.push(arr[i])
  }
  return array
}

console.log(insert(arr, item, index))
```

## 10

> 描述

统计数组 arr 中值等于 item 的元素出现的次数.

> 输入

`[1, 2, 4, 4, 3, 4, 3]` `4`

> 输出

`3`

> 代码

```javascript
const arr = [1, 2, 4, 4, 3, 4, 3]
const item = 4

const count = (arr, item) => {
  let count = 0
  for (let i =0; i < arr.length; i++) {
    if (arr[i] === item) {
      count++
    }
  }
  return count
}

console.log(count(arr, item))
```

## 11

> 描述

找出数组 arr 中重复出现过的元素 (不用考虑返回顺序).

> 输入

`[1, 2, 4, 4, 3, 3, 1, 5, 3]`

> 输出

`[1, 3, 4]`

> 代码

```javascript
const arr = [1, 2, 4, 4, 3, 3, 1, 5, 3]

const duplicates = (arr) => {
  const array = []
  for (let i = 0; i < arr.length; i++) {
    array.push(arr[i])
  }
  for (let i = 0; i < array.length; i++) {
    let count = 0
    for (let j = i + 1; j < array.length; j++) {
      if (array[i] === array[j]) {
        array.splice(j, 1)
        count++
        j--
      }
    }
    if (count === 0) {
      array.splice(i, 1)
      i--
    }
  }
  return array
}

console.log(duplicates(arr))
```

## 12

> 描述

为数组 arr 中的每个元素求二次方, 不要直接修改数组 arr, 结果返回新的数组.

> 输入

`[1, 2, 3, 4]`

> 输出

`[1, 4, 9, 16]`

> 代码

```javascript
const arr = [1, 2, 3, 4]

const square = (arr) => {
  const array = []
  for (let i = 0; i < arr.length; i++) {
    array.push(arr[i]**2)
  }
  return array
}

console.log(square(arr))
```

## 13

> 描述

在数组 arr 中, 查找值与 item 相等的元素出现的所有位置.

> 输入

`['a', 'b', 'c', 'd', 'e', 'f', 'a', 'b', 'c']` `'a'`

> 输出

`[0, 6]`

> 代码

```javascript
const arr = ['a', 'b', 'c', 'd', 'e', 'f', 'a', 'b', 'c']
const item = 'a'

const findAllOccurrences = (arr, item) => {
  const array = []
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === item) {
      array.push(i)
    }
  }
  return array
}

console.log(findAllOccurrences(arr, item))
```

## 14

> 描述

使用 parseInt 方法, 通过以下测试用例.

> 输入

`'12'` `'12px'` `'0x12'`

> 输出

`12` `12` `0`

> 代码

```javascript
const input1 = parseInt('12')
const input2 = parseInt('12px')
const input3 = parseInt('0x12')

const output1 = parseInt(input1)
const output2 = parseInt(input2)
const output3 = parseInt(input3)

console.log(output1, output2, output3)
```

## 15

> 描述

判断 val1 和 val2 是否完全等同.

> 代码

```javascript
const identity = (val1, val2) => {
  return val1 === val2
}
```

## 16

> 描述

实现一个打点计时器, 要求:

1. 从 start 到 end (包含 start 和 end), 每隔 100 毫秒 console.log 一个数字, 每次数字增幅为 1
2. 返回的对象中需要包含一个 cancel 方法, 用于停止定时操作
3. 第一个数需要立即输出

> 代码

```javascript
const count = (start, end) => {
  const cancel = () => {
    clearInterval(loop)
  }
  console.log(start)
  let count = 1
  const loop = setInterval(
    () => {
      console.log(start + count)
      count++
      if (start + count === end) {
        cancel
      }
    },
    100
  )
  return { cancel }
}
```

## 17

> 描述

实现 fizzBuzz 函数，参数 num 与返回值的关系如下:

1. 如果 num 能同时被 3 和 5 整除, 返回字符串 fizzbuzz
2. 如果 num 能被 3 整除, 返回字符串 fizz
3. 如果 num 能被 5 整除, 返回字符串 buzz
4. 如果参数为空或者不是 Number 类型, 返回 false
5. 其余情况, 返回参数 num

> 代码

```javascript
const fizzBuzz = (num) => {
  if (typeof num !== 'number') {
    return false
  }
  if (num % 15 === 0) {
    return 'fizzbuzz'
  }
  if (num % 3 === 0) {
    return 'fizz'
  }
  if (num % 5 === 0) {
    return 'buzz'
  }
  return num
}
```

## 18

> 描述

将数组 arr 中的元素作为调用函数 fn 的参数.

> 代码

```javascript
const argsAsArray = (fn, arr) => {
  return fn.apply(this, arr)
}
```

