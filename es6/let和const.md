# let和const

### 相比较于var

* ##### var没有块级作用域

* ##### var存在变量提升

  * ##### 成为全局变量

* ##### 可以重复定义

### let和const

* ##### 不允许重复定义

* ##### 都有块级作用域

* ##### 都没有变量提升

* ##### 暂时性死区

  * ``` js
    console.log(data) //ReferenceError
    let data = 123
    ```

* ##### let

  * ##### 声明的值可以改变

* ##### const

  * ##### 声明的值不能改变

  * ##### 引用类型的属性可以改变

### 一个经典的案例

```js
//首先使用var
for (var i=0; i<10;i++){
    setTimeout(() => {
        console.log(i)
    },1000)
}
//再使用let
for (let j=0; j<10;j++){
    setTimeout(() => {
        console.log(j)
    },1000)
}
```

![1640951865435](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1640951865435.png)



### 这种原因就是var没有块级作用域，最后的i值全部变成了10

