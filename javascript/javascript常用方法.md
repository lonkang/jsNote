## Array

```javascript
let arr = [1, 3, 4, 0 ,3]
Array.isArray() // 判断是否是一个数组

.concat() // 连接多个数组 并返回结果
let c = [1, 23, 4].concat([2, 4])

.push() // 数组的最后添加元素
arr.push(3) // [1,3, 4,0, 3, 3]

.pop() // 删除数组中最后一个元素 并返回被删除的元素
arr.pop() //  [1,3, 4,0, 3]

.shift() // 删除数组中的第一个元素，
arr.shift() //  [3, 4,0, 3]

.unshit() // 向数组的开头添加一个或更多元素，并返回新的长度。
arr.unshilt(1) // [1, 3, 4,0, 3]

.indexOf() // 搜索数组中的元素，并返回它所在的位置。
arr.indexOf(1) // 0 

.find() // 查找数组中有没有该元素

.findIndex // 查找到数组中的元素并返回索引值

.join("字符串"); // 返回的是一个字符串
arr.join(',') // '1, 3, 4, 0, 3'

.sort() // 排序
arr.sort() //  [0, 1, 3, 3, 4]

.reverse() // 翻转数组
arr.reverse() // [4, 3, 3, 1, 0]

.slice() //  选取数组中的一部分进行截取
let a = arr.slice(1) // [3, 3, 1, 0]
.splice(index, 删除多少元素, 要添加的元素) // 从数组中添加或修改或删除元素。
// 删除
arr.splice(0 , 1)
// [3, 3, 1, 0]

// 修改
arr.splice(0, 1, 5)
// [5, 3, 1, 0]
// 添加
arr.splice(1, 0, 1, 2, 3, 4 )
// [5,1, 2, 3, 4, 3, 1, 0]

.forEach() // 遍历数组用---相当于for循环
arr.forEach((value, index) => {})

.map() // 通过指定函数处理数组的每个元素，并返回处理后的数组。
arr.map((value, index, arr) => {
    return value + 1
})

.some() // 检测数组元素中是否有元素符合指定条件。
// 如果有一个元素满足条件，则表达式返回true , 剩余的元素不会再执行检测。
// 如果没有满足条件的元素，则返回false。
arr.some((value, index) => {
 return value > 2
})

.every // 检测数组元素的每个元素是否都符合条件。
// 所有元素都满足条件才返回 true
arr.every((value, index) => {
    return value > 2
})

.filter() // 检测数组元素，并返回符合条件所有元素的数组。
arr.filter((value, index) => {
    return value > 5
})
.find() // 寻找满足条件的第一个值
arr.find(ele => ele > 5)

.reduce((累计值, 当前值, 当前索引, 当前数组) => {} , 初始值) // 计算值
arr.reduce((pre, value) => {
    return pre + value
}, 0)
// 11
```

## Boolean

```javascript
Boolean.tostring() // 将布尔值转换为字符串
Boolean.valueOf() // 返回 Boolean 对象的原始值。
```

## Date

```javascript
通过 new Date可以获取当前时间
var d = new Date()

var dt = Date.now() // 获取毫秒值

var d = Date.parse("March 21, 2012"); // 返回1970年1月1日午夜到指定日期（字符串）的毫秒数。


var dt = new Date()

// 获取年份
   dt.getFullYear()
// 获取月份
   dt.getMonth() + 1 //是0开始的 真实的月份是需要加1的
// 获取日期
   dt.getDate()
// 获取小时
   dt.getHours()
// 获取分钟
   dt.getMinutes()
// 获取秒
   dt.getSeconds()

// 获取星期
   dt.getDay() //星期从0开始的
// 返回 1970 年 1 月 1 日至今的毫秒数。
   dt.getTime()

   dt.toDateString();//日期
   dt.toLocaleDateString();//日期
   dt.toTimeString();//时间
   dt.toLocaleTimeString();//时间
   dt.valueOf();//毫秒


// js转换时间
/**
 * Created by Administrator on 2017-09-13.
 */
//格式化后的指定格式的日期和时间---封装一个函数

/**
 * 获取指定格式的时间
 * @param dt 日期的对象
 * @returns {string} 返回的是字符串的日期时间
 */
function getDate(dt) {
    //获取年
    var year = dt.getFullYear();
    //获取月
    var month = dt.getMonth() + 1;
    //获取日
    var day = dt.getDate();
    //获取小时
    var hour = dt.getHours();
    //获取分钟
    var minute = dt.getMinutes();
    //获取秒
    var second = dt.getSeconds();
    month = month < 10 ? "0" + month : month;
    day = day < 10 ? "0" + day : day;
    hour = hour < 10 ? "0" + hour : hour;
    minute = minute < 10 ? "0" + minute : minute;
    second = second < 10 ? "0" + second : second;
    return year + "年" + month + "月" + day + "日 " + hour + ":" + minute + ":" + second;
}
```

## Math

```javascript
// 01 向上取整
Math.ceil()
// 02 向下取整
Math.floor()
// 03 绝对值
Math.floor()
// 04 π
Math.PI
// 05 随机数
Math.random()
// 06 最大值
Math.max(1, 2, 3, 4, 5)
// 07 最小值
Math.min(1, 2, 3, 4, 5)
```

## Number

```javascript
toExponential(x)	// 把对象的值转换为指数计数法。
toFixed(x)	// 把数字转换为字符串，结果的小数点后有指定位数的数字。
toPrecision(x)	// 把数字格式化为指定的长度。
toString()	// 把数字转换为字符串，使用指定的基数。
valueOf() // 返回一个 Number 对象的基本数字值。
```

## Object

```javascript
Object.is() // 判断两个值是否相等
Object.assagin() // 合并两个对象
Object.defineProperty()
Object.definePropertires()
Object.getOwnPropertyDescriptor() // 获取某个对象属性的描述属性
Object.getOwnPropertyDescriptors() // 返回指定对象所有自身属性（非继承属性）的描述对象。
Object.create() // 创建一个对象的原型
Object.setPrototypeOf() // 
// 格式
Object.setPrototypeOf(object, prototype)

// 用法
const o = Object.setPrototypeOf({}, null);
Object.getPrototypeOf()
Object.keys()
Object.values()
Object.entries()
Object.fromEntries()

```

## String

```javascript

.length //------>字符串的长度
.charAt(索引) //返回值是指定索引位置的字符串,超出索引,结果是空字符串
.fromCharCode(数字值,可以是多个参数) //返回的是ASCII码对应的值
.concat(字符串1,字符串2,...) // 返回的是拼接之后的新的字符串
.indexOf(要找的字符串,从某个位置开始的索引) //返回的是这个字符串的索引值,没找到则返回-1
.lastIndexOf(要找的字符串) // 从后向前找,但是索引仍然是从左向右的方式,找不到则返回-1
.replace("原来的字符串","新的字符串") //用来替换字符串的
.slice(开始的索引,结束的索引) // 从索引5的位置开始提取,到索引为10的前一个结束,没有10，并返回这个提取后的字符串 .
.split("要干掉的字符串",切割后留下的个数) // 切割字符串
.substr(开始的位置,个数) // 返回的是截取后的新的字符串 .substr(start, length)
.substring(开始的索引,结束的索引) // 返回截取后的字符串,不包含结束的索引的字符串 .substring(from, to)
.toLocaleLowerCase() // 转小写
.toLowerCase() // 转小写
.toLocaleUpperCase() // 转大写
.toUpperCase() // 转大写
.trim() // 干掉字符串两端的空格


slice()和split()的区别
splice是用来提取字符串的片断，并在新的字符串中返回被提取的部分。
split是把字符串分割为字符串数组。
let str = 'hello world'
let a = str.splice(1, 3) // 'el'
let b = str.split(' ') ['hello', 'world']
substr()和substring()的区别
substr 是从起始索引号提取字符串中指定数目的字符。
substring 是提取字符串中两个指定的索引号之间的字符。
let c = str.substr(1, 3) // 'ell'
let d = str.substring(1, 3) // 'el'


```

## RegExp

```javascript
// 元字符：
. // 匹配除了\n以外的任意一共字符 

[] 表示的是:范围
[0-9] // 表示的是0到9之间的任意的一个数字,  "789" [0-9]
[1-7] // 表示的是1到7之间的任意的一个数字
[a-z] // 表示的是:所有的小写的字母中的任意的一个
[A-Z] // 表示的是:所有的大写的字母中的任意的一个
[a-zA-Z] // 表示的是:所有的字母的任意的一个
[0-9a-zA-Z] // 表示的是: 所有的数字或者是字母中的一个
[] // 另一个含义: 把正则表达式中元字符的意义干掉    [.] 就是一个.

| // 或者  [0-9]|[a-z] 表示要么是一共数字，要么是一共字母

() // 分组 或者是提高优先级 [0-9]|(a-z)|[A-Z]
//  ([0-9])([1-5])([a-z]) 三组, 从最左边开始计算

// 限定符
* // 表示的是 前面的表达式出现0次到无数次 
+ // 表示的是 前面的表达式出现1次到无数次
? // 表示的是 前面的表达式出现0次到1次

{} // 限定前面的表达式出现几次
{0, } // 表示前面的表达式出现0次到多次 和*一样
{1, } // 表示前面的表达式出现0次到多次 和+一样
{0, 1} // 表示前面的表达式出现0次到多次 和？一样
{5, 10} // 表示前面的表达式出现5次到10次 
{5}  // 表示前面的表达式出现5次
{, 10} // 错误
 
^ // 表示的是以什么开始,或者是取非(取反) ^[0-9] 以数字开头
^[a-z] 以小写字母开始
[^0-9] 取反,非数字
[^a-z] 非小写字母
[^0-9a-zA-Z_]

$ // 表示的是以什么结束   [0-9][a-z]$  必须以小写字母结束 
^[0-9][a-z]& // 相当于是严格模式   "3f2432e"  "4f"
 
\d // 数字中的任意一个
\D // 非数字中的任意一个
\s // 空白符
\S // 非空白符
\W // 非特殊符号 包括(_)
\W // 特殊符号 不包括(_)
\b // 单词边界

// 邮箱正则
let reg = /^[0-9a-zA-Z_.-]+[@][0-9a-zA-z_.-]+([.][a-zA-z]+){1, 2}/

/g // 代表全局匹配 
/i // 代表忽略大小写
/m // 多行匹配

// 字符串的 match方法
// match() 方法可在字符串内检索指定的值，或找到一个或多个正则表达式的匹配。

// replace()方法 可以替换与正则表达式匹配的字符串

// test() 方法 可以测速匹不匹配字正则

// exec() 在字符串中匹配搜索， 返回结果数组 和 match()类似 但是 mathch不要循环 exec() 需要遍历

// search() 在字符串中进行匹配 返回第一个值的索引值

// split() 把字符串切割为数组 

var str="中国移动:10086,中国联通:10010,中国电信:10000";
//把里面所有的数字全部显示出来
var array=str.match(/\d{5}/g);
console.log(array);

 var str = "123123@xx.com,fangfang@valuedopinions.cn 286669312@qq.com 2、emailenglish@emailenglish.englishtown.com 286669312@qq.com...";
var array = str.match(/\w+@\w+\.\w+(\.\w+)?/g);
console.log(array);
 
// 提取这里的日
// 进行分组 然后可以获取相应的组
var str="2017-11-12";
var array=str.match(/(\d{4})[-](\d{2})[-](\d{2})/g);
//console.log(array);
//正则表达式对象.$3
console.log(RegExp.$3);


var email="shuaiyangtaishuaile@itcast.com.cn";
email.match(/([0-9a-zA-Z_.-]+)[@]([0-9a-zA-Z_-]+)(([.][a-zA-Z]+){1,2})/);
console.log(RegExp.$1);//用户名
console.log(RegExp.$2);//126
console.log(RegExp.$3);//域名
 

 
// replace

var str="小苏好帅哦,真的是太帅了,帅,就是真帅";
str=str.replace(/帅/g,"猥琐");
console.log(str);

var str="  哦买噶的    ,太幸福了  ";
str=str.trim();
console.log("==="+str+"===");


var str = "  哦买噶的    ,太幸福了  ";
str = str.replace(/\s+/g, "");
console.log("===" + str + "===");


//所有的h都替换成S
var str="HhpphH";//SSppSS
str=str.replace(/[h]/gi,"S");
console.log(str);

var reg = new RegExp(/[h]/gi);
var str = "HhpphH";//SSppSS
str = str.replace(reg, "S");
console.log(str);

 

 var str = "中国移动:10086,中国联通:10010,中国电信:10000";
//把里面所有的数字全部显示出来
// var array = str.match(/\d{5}/g);
// 正则表达式对象.exec方法传入字符串
var reg=/\d{5}/g;
var array=reg.exec(str);
console.log(array);
console.log(reg.exec(str));
console.log(reg.exec(str));
console.log(reg.exec(str));

 var result=reg.exec(str);
 while(result!=null){
	console.log(result);
	result=reg.exec(str);
  }



//    var str = "中国移动:10086,中国联通:10010,中国电信:10000";
//    var reg=/\d{5}/g;
//    //通过正则表达式匹配这个字符串
//    var array=reg.exec(str);
//    console.log(array);
//    console.log(reg.exec(str));
//    console.log(reg.exec(str));
//    console.log(reg.exec(str));//null
//


    var str = "中国移动:10086,中国联通:10010,中国电信:10000";
    var reg=/\d{5}/g;
    //通过正则表达式匹配这个字符串
    var array=reg.exec(str);
    while (array!=null){
      //输出匹配的内容
      console.log(array[0]);
      array=reg.exec(str);
    }

```

## Window

```

```

