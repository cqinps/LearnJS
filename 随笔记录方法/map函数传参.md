# map函数默认传参

```js
let data = [1,2,3,4,5]

function fn(...args){
    console.log(args)
}

data.map(fn)   //输出👇
```

![1641361432621](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1641361432621.png)

##### map函数一共默认传三个参数，从左至右 currentValue   index   array 所以map支持值传入一个函数/方法，传参的步骤交给map

### 但是有的时候就会出现一些问题

```
let data = ['1','2','3']
data.map(parseInt); // 1,NaN,NaN
```

因为，parseInt是需要两个参数，第二个大多数情况下我们不传参数
parseInt(string, radix);
 	string
 		要被解析的值。如果参数不是一个字符串，则将其转换为字符串(使用  ToString 抽象操作)。字符串开头 	     的空白符将会被忽略。
 	radix 可选
         从 2 到 36，表示字符串的基数。例如指定 16 表示被解析值是十六进制数。请注意，10不是默认值！

​		如果传入参数是0 或  undefined 或 不传  默认以10进制解析,其他情况返回NaN



这样在map函数中，会给parseInt传两个参数，

parseInt(currentValue,index)   map默认传的第三个array参数不传

```js
parseInt('1',0)  默认以10进制解析
parseInt('2',1)	 返回NaN
parseInt('3',2)  以二进制解析，但是3不属于二进制，同样返回NaN
```

