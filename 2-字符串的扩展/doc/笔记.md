##### 字符串扩展

1. 模版字符串

   之前单引号或者双引号定义字符串的缺点：

   1. 不能换行

   2. 有时候会做大量字符串的拼接，麻烦，还容易出错

      

   es6用一对反引号(\`  \`)定义字符串，特点：

   1. 任何换行

   2. 不需要做字符串拼接工作，直接在字符串中嵌入变量，

      嵌入的语法是:

      ```js
      ${变量名|运算|调用函数}
      ```

      **直接嵌入变量**：

      ```js
      let y = 2018,
      		m = 12,
      		d = 26;
      let str = `${y}年${m}月${d}日是毛爷爷的生日`;
      
      console.log(str);
      ```

      **做一些简单的运算（加、减、乘、除、模、三目之类的）**:

      ```js
      let age = 20;
      let str = `狗蛋今年${age * 2},${age >= 18 ? '成年':'未成年'}`;
      console.log(str);
      ```

      **调用函数**：

      ```js
      let name = "rose";
      function capitalize(str) {
        return str.charAt(0).toUpperCase() + str.slice(1).toLowerCase();
      }
      let str = `我是${capitalize(name)}`;
      console.log(str);
      ```

      

2. 几个方法

   includes(str)：

   检测一个字符串是否包含另一个字符串，如果包含，返回true，否则返回false

   startsWith(str,[index=0]): 检测字符串是否已某个字符串开头

   ```js
   let str = 'https://www.xxx.com';
   console.log(str.startsWith('https'));
   ```

   endsWith(str):检测字符串是否已某个字符串结尾

   ```js
   let filename = 'c://users/desktop/1.gif';
   if(filename.endsWith('.jpg')) {
     console.log('jpg');
   }else if(filename.endsWith('.png')) {
     console.log('png');
   }else if(filename.endsWith('.gif')) {
     console.log('gif');
   }else if(filename.endsWith('.webp')) {
     console.log('webp');
   }else {
     console.log('其它');
   }
   ```

   repeat

   















