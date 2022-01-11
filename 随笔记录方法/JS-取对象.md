# JavaScript   一层一层取对象报错

### 方法一    <font color='red'>?.</font>

###  ?.  介绍

###  可选链操作符

* ##### 通过连接的对象的引用或函数可能是 `undefined` 或 `null` 时，可选链操作符提供了一种方法来简化被连接对象的值访问。 



#### 1.当取一个存在的对象，以及一个存在对象的一个不存在属性时候

![1641122986613](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1641122986613.png)

#### 2. 当去一个存在的对象的一个不存在属性的一个属性时候会报错

![1641123120959](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1641123120959.png)

#### 3.这个时候 使用  ?.  操作符

![1641123374044](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1641123374044.png)

####  <font color='red'>意思和 && 类似</font>



---



### 方法二  定义一个函数，兼容各种浏览器

```js
function safeGet(obj,path) {
    items = path.split('.')
    for (const item of items) {
        if(obj){
            obj = obj[item]
        }
    }
    return obj
}
```

##### 只会判断到，null，或者undefined一层，就返回了

