> - ### npm网站查询 [这个是npm网站](https://www.npmjs.com/)
>
> - ### supergent 模块的引入
>
>   - #### 这里引入的方式是局部引入 
>
>     - ##### 代码是npm install --save superagent

![image-20200309123436136](C:\Users\梦神\AppData\Roaming\Typora\typora-user-images\image-20200309123436136.png)



>  ### - @Type/superagent模块
>
> - npm i -save @type/superagent
>   - 原理:__TS直接引用js文件,是不行的*__
>   - 



### 引入superagent模块

> `*import* superagent *from* "superagent";`
>
> ```ts
> // TS直接引用js文件,是不行的
> // te -> .d.ts 翻译文件 -> js
> 
> import superagent from "superagent";
> 
> console.log("hello ~ ts");
> 
> class Crowller {
>   private secret = "secretKey";
>   private url = `http://www.dell-lee.com/Typescript/demo.html?secret=${this.secret}`;
>   private rawHtml = "";
> 
>   // console.log("constructor:构造器");
>   // 构造器
>   async getRawHtml() {
>     const result = await superagent.get(this.url);
>     this.rawHtml = result.text;
>     console.log(result.text);
>   }
>   constructor() {
>     this.getRawHtml();
>   }
> }
> 
> const crowller = new Crowller();
> 
> 
> ```
>
> 





>  这其中把全局ts-node删除了, 然后局部安装了tsnode ,具体用意也不太清楚 . 
>
> 总之安装局部ts-node之后, 初始化了文件夹 __`npm init -y`__
>
> - 多了个__`package.json`__,
>   - 又初始化 TS 
>     - 多了个__`tsconfig.json`__??
>   - 初始化TS命令 __`tsc --init`__

> - 然后在里面配置启动命令
> - __`"dev": "ts-node ./crowller.ts"`__
> - 
>
> 

