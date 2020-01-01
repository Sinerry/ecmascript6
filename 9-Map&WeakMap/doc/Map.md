##### Map

以key-value的格式存储一组无序的数据，这个特点与之前键值对的对象存储特点一致，只不过之前的对象的key只能字符串类型，不能是其它数据类型，而es6的Map结构，它的key可以任何数据类型



1. 创建

   

   创建空map

   ```js
   let map = new Map()；
   map.set('name','狗蛋');
   map.set('age',18);
   map.set('sex','male');
   map.set(new Date(),'2020-01-01');
   map.set(document,'haha');
   map.set(undefined,'123');
   map.set(true,false);
   map.set(function(){},'北京');
   map.set([],'数组');
   map.set({},'对象');
   map.set(/\s+/,'正则');
   map.set(1,'数字');
   map.set(Symbol(),'独一无二');
   ```

2. 属性和方法

   属性：

   size：map中键值对的 对 数

   方法：

   set：

   添加/新增： 如果key不存在

   修改：key存在

   

   get：获取，根据key获取value，

   如果key不存在，返回undefined

   

   delete：

   删除，根据key删除该组键值对

   返回布尔值，如果删除成功，返回true，否则返回false

   

   has：检测map中是否含有某个键

   如果含有，返回true，否则返回false

   

   clear：清空

   

   forEach：遍历map

   ```js
   map.forEach((v,k) => {
     console.log(v,k)
   });
   ```

   

   keys：返回map所有key的迭代（遍历）器

   遍历map所有的key：

   ```js
   for(let k of map.keys()) {
     console.log(k);
   }
   ```

   

   values：返回map所有value的迭代（遍历）器

   遍历map所有的value：

   ```js
   for(let v of map.values()) {
     console.log(v);
   }
   ```

   

   entries：返回map所有key-value的迭代（遍历）器

   遍历map所有的key-value：

   ```js
   for(let [k,v] of map.entries()) {
     console.log(k,v);
   }
   ```

   

   

   

   

   









##### WeakMap









