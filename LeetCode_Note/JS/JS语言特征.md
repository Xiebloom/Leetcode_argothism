#  JS语言特征



## 1  字符串不可变

 在 JavaScript 中， 字符串  的值是  不可变的 ，这意味着一旦字符串被创建就不能被改变。

 例如，下面的代码：

```js
 var myStr = "Bob";

 myStr[0] = "J";
```

 是不会把变量  myStr  的值改变成 "Job" 的，因为变量  myStr  是不可变的。注意，这  **并不**  意味着  myStr  永远不能被改变，只是字符串字面量  *string literal*  的各个字符不能被改变。改变  myStr  中的唯一方法是重新给它赋一个值，就像这样：

```js
 var myStr = "Bob";

 myStr = "Job";
```



## 2 对象内部的排序规律

对象内部自动排序，
按照testNum = [4,4,4,4,3,2,1,1]生成对象后，会变成{ 1:2, 2:1, 3:1, 4:4} ，
即按照元素名自动排序



## 3 数组的赋值

```js
        //函数传递数组是否会改变原来的值
        //ANS 会，并且数组浅复制也会
        arr = grid;
        function changeValue(arr){
            arr[0] = 5;
            return ;
        }
        changeValue(arr);	
        console.log(arr);	//[5,array[3],arrar[3]]
        console.log(grid);	//[5,array[3],arrar[3]]
```

