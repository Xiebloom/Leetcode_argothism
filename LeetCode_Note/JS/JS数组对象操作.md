# 系统函数



## 1  对Obj操作

#### 取出所有对象的值

`let arr = Object.values(obj);`



## 2  Array相关杂项

#### 2.1 对数组内的每个元素操作

```    js
        sortArr.forEach((item, index) => {
            //操作内容
        })
```

#### 2.2 sort / splice 会改变原数组吗？ 未初始化的数组长度是多少？ 是否占位置？

```js
        //SORT会改变原数组么 会 
        var arr = [1,2,3,4,1];
        arr.sort( (a,b) => a-b);
        console.log(arr)

        //未初始化的数组的长度是多少？
        var queue =[[],[]];
        console.log( queue.length);
        //Ans: 0;  但是空对象占位置

        //splice改变原数组吗？  
        var sreturn = arr.splice(1,1);
        console.log(sreturn);
        //改变 
```



## 3  数组对象

#### 3.1  创建数组的两种方式

  ①  字面量 `var arr1 = [1,2,3];`

  ②  `var arr1 = new Array(2)	// 创建一个数组长度为2的数组`

  ③ `var arr1  =  new Array(2, 3)	//等价于var arr1 = [2, 3]`

#### 3.2  检测是否为数组

* instanceof	运算符，可用来检测是否为数组

#### 3.3  添加/删除数组元素的办法

* push()	//在数组末尾，添加一个或多个数组元素。
  * 功　能：追加新数组元素
  * 参　数：直接写要添加的值
  * 返回值：新数组的长度
  * 测试后注意点：原数组也会变化

* unshift()   //在数组的先头追加元素
  * 在先头追加元素
  * 直接写值
  * 新数组的长度			

* 删除数组元素

  * pop()	
    * 删除最后的元素
    * 不需要参数
    * 返回值为被删除掉的元素
  * shift()  
    * 删除第一个元素
    * 无参数
    * 返回值为新的长度

#### 3.4  数组翻转和排序

  * reserve()

    * 翻转数组元素
    * 不需要参数
    * 返回值为新的数组，同时原数组也翻转了。

  * sort()

    * 冒泡排序

    * 不需要参数

    * 返回新数组

    * 并不是按照数值，而是按照字符串顺序排序

    * 示例及升序排序写法

      ※  **原数组会受到影响**


          arr = [1,3,5,5,12,55];
          arr.sort();
          console.log(arr);   //[1,12,3,5,55] 按的是字符串顺序
      
          arr.sort(function(a,b){
              return a - b;       //升序排列
          });
          console.log(arr);   //[1,3,5,5,12,55]

#### 3.5  字符串索引

* arr.indexOf( '查找对象' )；
* arr.lastindexOf( '' );

 #### 3.6  将数组转化为字符串

* toString() 
  * 转化成字符串，以逗号分割
* join( '分隔符' )
  * 转化成字符串，以自己规定的分隔符分割，默认是逗号

 #### 3.7  数组连结：concat

* 强烈建议用 + or +=, 不要用这个

#### 3.8  数组截取 : arr.slice( start, end )

#### 3.9  数组删除： arr.splice(开始索引，删除个数)

* 功能：删除数组内的元素

* 参数：开始索引，元素个数

* 返回值：**被删除的元素**

  ※  原数组会受到影响

* 也可以插入 

  ``arr.splice( 插入索引， 0， 插入元素)``

### 3.10 数组深拷贝 Array.from()

* 拷贝完你是你，我是我，互不相影响





## ASCII码值计算

```js
        console.log(parseInt('z'-'s')); //NaN
```

