# Object.defineroperty  和Object.defineroperties

## 用法Object.defineroperty 

#### 给object1添加一个属性名为property1的属性

```js
Object.defineProperty(object1, 'property1', {  
  configurable: fasle,
  enumerable :false,
  value :undefined,
  writable :fasle,
  get(){
    return value
  }
  set(xxx){
    value = xxx
  }	
});
```



- `configurable`

  **默认为** **false**。

  当且仅当该属性的 `configurable` 键值为 `true` 时，该属性的描述符才能够被改变，同时该属性也能从对应的对象上被删除。 

- `enumerable`

  **默认为 false**

  当且仅当该属性的 `enumerable` 键值为 `true` 时，该属性才会出现在对象的枚举属性中。 。

   <font color='red'> 定义了对象的属性是否可以在 [`for...in`] 循环和 [`Object.keys()`]中被枚举。 </font>

  数据描述符还具有以下可选键值：

- `value`

   **默认为 undefined**

  该属性对应的值。可以是任何有效的 JavaScript 值（数值，对象，函数等）。

- `writable`

  **默认为 false。**

  当且仅当该属性的 `writable` 键值为 `true` 时，属性的值，也就是上面的 `value`，才能被`赋值运算符` 改变。 

  

---

### 存取描述符还具有以下可选键值：

- `get`

  **默认为 undefined**

  属性的 getter 函数，如果没有 getter，则为 `undefined`。当访问该属性时，会调用此函数。执行时不传入任何参数，但是会传入 `this` 对象（由于继承关系，这里的`this`并不一定是定义该属性的对象）。该函数的返回值会被用作属性的值。 

- `set`

  **默认为 undefined**

  属性的 setter 函数，如果没有 setter，则为 `undefined`。当属性值被修改时，会调用此函数。该方法接受一个参数（也就是被赋予的新值），会传入赋值时的 `this` 对象。 

-  <font color='red'>如果一个描述符不具有 `value`、`writable`、`get` 和 `set` 中的任意一个键，那么它将被认为是一个数据描述符。如果一个描述符同时拥有 `value` 或 `writable` 和 `get` 或 `set` 键，则会产生一个异常。 </font>

## Object.defineroperties

### 和Object.defineroperty  用法类似

Object.defineroperties(object1,{

 <font color='red'>这个就是把 defineroperty，的后面的两个参数包裹起来，并且可以定义多个</font>

})

<img src="D:\Users\lenovo\Desktop\1640936063184.png" alt="1640936063184" style="zoom:150%;" />

