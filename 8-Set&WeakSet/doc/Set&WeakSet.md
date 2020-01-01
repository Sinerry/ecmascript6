##### ES6新增的两种数据结构




##### Set

1. 概念：

   集合，存储一组**唯一**，**无序**数据的容器

   ​	唯一：不重复

   ​	无序：

   ​			本质：

   ​			添加的顺序与取值的顺序不一致

   ​		

   ​			代码层面： 

   ​			不能用下标取值(没有下标这一说)

   

   ​	有序：

   ​				 添加的顺序与取值的顺序一致（数组，字符串）

    				能用下标取值(没有下标这一说)

   

2. 创建

创建空集合

```js
let set = new Set();
console.log(set);
```



```js
let set = new Set(iterable_object);


let set1 = new Set([1,2,3,4,5]);
console.log(set1);



let set2 = new Set('hello');
console.log(set2)



let divs = document.getElementsByClassName('dachui');
let set3 = new Set(divs);
console.log(set3)
```



集合的特性

```js
let set = new Set([1,1,1,2,2,3,3,4]);
// 唯一性
console.log(set);//  {1, 2, 3, 4}
// 无序性
console.log(set[0]);// undefined
console.log(set[1]);// undefined
console.log(set[2]);// undefined
```



使用集合对数组快速去重

```js
let array = [3,3,5,5,2,1,3,2,5,2];
console.log([...new Set(array)]);
```



集合的属性和方法

属性：

size： 集合中元素的个数，跟数组的length属性一样

```js
let set = new Set('world');
console.log(set.size);// 5
```

方法：
add(item):    添加

delete(item)： 删除

has(item)： 是否含有

clear() ： 清空集合

forEach()：遍历集合

keys()：      返回集合（成员）的迭代（遍历）器

values()：   返回集合（成员）的迭代（遍历）器

entries：     返回集合（成员）的迭代（遍历）器



```js
let set = new Set();
// 添加
set.add('w');
set.add('o');
set.add('r');
set.add('l');
set.add('d');

// 删除
set.delete('r');

// 包含
console.log(set.has('w'));// true
console.log(set.has('ww'));// false

// 清空
// set.clear()

// 遍历
set.forEach(item => {
	console.log(item);
});

// 把集合转成迭代器对象
console.log(set.keys());
console.log(set.values());

```



注意： 

1. 集合中元素不能获取，也不能修改

2. 集合可以被for of遍历

   ```js
   console.log(set[Symbol.iterator]);
   for(let item of set) {
     console.log(item);
   }
   ```

3. set结构的键和值是同一个值





















##### WeakSet

只能存储object类型，否则会报错，功能比Set要弱

弱在哪些地方呢？

1. WeakSet只能存储object类型，Set可以存储任何数据类型
2. 没有size属性
3. 只用add，has，delete三个方法
4. 不可迭代

```js
let ws = new WeakSet();
ws.add([1,2]);
ws.add({name:'狗蛋'});
ws.add(new Date());
ws.add(document);

console.log(ws.size);// undefined

for(let item of ws) {// 报错，WeakSet集合不可迭代
  
}
```

































































##### Map







