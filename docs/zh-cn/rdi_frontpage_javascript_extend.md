##  rdiframework-extend.js

---

```

javascript
<!--rdiframework-area.js存放区域编码的一个常量。由于rdiframwork-extend.js里面的getPersonInfo18()方法需要调用这个常量，
所以在rdiframwork-extend.js之前引入。如果不需要用到这个方法也可以不引入rdiframwork-area.js-->
<script type="text/javascript" src="framework/js/rdiframwork-area.js" ></script>
<script type="text/javascript" src="framework/js/rdiframwork-extend.js" ></script>

```

### 该javaScript库主要包括了如下模块：

#### 1、手机号码校验
#### 2、身份证校验
#### 3、邮箱校验
#### 4、字符串常用类
#### 5、简单四则运算
#### 6、正则表达式生成工具类
#### 7、日期工具
#### 8、url工具
#### 9、数组工具类
#### 10、对象工具类

### 1、手机号码校验； 

- [x]  //电话号码
	
>isPhoneCallNum: function(input)

- [x] //电信手机号码
  
>  isChinaTelecomPhoneNum: function(input)

- [x]	//中国联通
	
>	isChinaUnicomPhoneNum: function(input) 

- [x]	//中国移动
	
>	isChinaMobilePhoneNum: function(input) 

- [x]	 //手机号码

>	isPhoneNum: function(input)

- [x]	//手机号码简单校验，只校验长度

>	isPhoneNumBySize: function(input) 

### 2、身份证校验； 

- [x]	//18位身份证简单校验

>	isSimpleIdCard18: function(idCard) 

- [x]	//15位身份证简单校验

>	isSimpleIdCard15: function(idCard) 

- [x]	//18位身份证校验码校验

>	checkCode: function(idCard) 

- [x]	//18位身份证严格校验

>	isIdCard18: function(idCard) 

- [x]	//根据18身份证号码获取人员信息

>	getPersonInfo18:function(idCard)

```javascript
//Demo
RDIFrameworkExtend.IdCardUtils.getPersonInfo18('350624199506094038');
```
```
//结果
{
	address: "福建省 漳州市 诏安县",
	sex: "男",
	birthday: "1995年06月09日",
	age: 23
}
```

### 3、邮箱校验； 

- [x] 邮箱校验

>	isEmail: function(input)

### 4、字符串常用类； 

- [x]	空字符串

>	isEmpty: function(input) 

- [x] 不是空字符串

> 	isNotEmpty: function(input) 

- [x] 空字符串，可为空格

> 	isBlank: function(input) 

- [x] 不是空字符串,空格也算空字符串
> isNotBlank: function(input) 

- [x] 去掉字符串两边的空格
>trim: function(input) 

- [x] 若为null则转为''	
> trimToEmpty: function(input) 

- [x] 以某个字符串开头		
> startsWith: function(input, prefix) 

- [x] 以某个字符串结尾
> endsWith: function(input, suffix) 

- [x] 包含某个子串
>contains: function(input, searchSeq) 

- [x] 判断字符串是否相等
>equals: function(input1, input2) 

- [x]	判断字符串是否相等，不区分大小写
>equalsIgnoreCase: function(input1, input2) 

- [x] 是否包含空白字符
>containsWhitespace: function(input) 

- [x]	//生成指定个数的字符
>		repeat: function(ch, repeatTimes) 

- [x]	删除空白字符
>	deleteWhitespace: function(input) 

- [x] 右侧补全
>ightPad: function(input, size, padStr) 

- [x] 左侧补全
>leftPad: function(input, size, padStr) 

- [x]//首小写字母转大写
	
>	capitalize: function(input) 

- [x]	//首大写字母转小写

>	uncapitalize: function(input) 

- [x]	//大写转小写，小写转大写

>	swapCase: function(input) 

- [x]	//统计含有的子字符串的个数

>	countMatches: function(input, sub) 

- [x]	//只包含字母

>	isAlpha: function(input) 

- [x]	//只包含字母、空格

>	isAlphaSpace: function(input) 

- [x]	//只包含字母、数字

	>	isAlphanumeric: function(input) 
- [x]	//只包含字母、数字和空格

	>	isAlphanumericSpace: function(input) 
- [x]	//数字
	
>	isNumeric: function(input) 

-- [x]	//小数
	
>	isDecimal: function(input) 

- [x]	//负小数
	
>	isNegativeDecimal: function(input) 

- [x]	//正小数
	
>	isPositiveDecimal: function(input) 

- [x]	//整数
	
>	isInteger: function(input) 

- [x]	//正整数

>	isPositiveInteger: function(input) 

- [x]	//负整数

>	isNegativeInteger: function(input) 

- [x]	//只包含数字和空格
  
> 	isNumericSpace: function(input) 

- [x] 是否为空白字符
>   sWhitespace: function(input) 

- [x] 是否全为小写字母
>  isAllLowerCase: function(input) 

- [x]	是否全为大写字母
>  sAllUpperCase: function(input) 

- [x]	字符串为空时，默认值
> defaultString: function(input, defaultStr) 

- [x]	字符串为空时，默认值
>defaultIfBlank: function(input, defaultStr) 

- [x]	字符串为空时，默认值
>defaultIfEmpty: function(input, defaultStr) 

- [x]	//字符串反转
>	reverse: function(input) 

- [x]	//删掉特殊字符(英文状态下)
>	removeSpecialCharacter: function(input) 

- [x]	//只包含特殊字符、数字和字母（不包括空格，若想包括空格，改为[ -~]）
>	isSpecialCharacterAlphanumeric: function(input) 

- [x]		/**
		 * @param {String} message
		 * @param {Array} arr
		 * 消息格式化
		 */
    
 >	format: function(message, arr) 
```

//demo
var message='我是{0}开发{1}';
var arr=['java','工程师'];
RDIFrameworkExtend.StringUtils.format(message,arr);
```
```
//结果
我是java开发工程师
```

- [x]	/**

		 * 把连续出现多次的字母字符串进行压缩。如输入:aaabbbbcccccd  输出:3a4b5cd
		 * @param {String} input
		 * @param {Boolean} ignoreCase : true or false 
		 */
	
>	compressRepeatedStr: function(input, ignoreCase) 
- [x]	//中文校验

>	isChinese: function(input) 

- [x]	//去掉中文字符
	
>	removeChinese: function(input) 

- [x]	//转义元字符

>	escapeMetacharacter: function(input) 

- [x]	//转义字符串中的元字符
>		escapeMetacharacterOfStr: function(input) 

- [x]	//中文转为unicode编码

>	chineseToUnicode: function(input) 

- [x]	 判断字符串是否是嵌套结构
  >   isNest: function(rule, str)

### 5、简单四则运算； 

- [x]   //加法

>	add: function(operandLeft, operandRight) 

- [x]   //减法
>	subtract: function(operandLeft, operandRight) 

- [x]     //乘法
>	multiply: function(operandLeft, operandRight)

- [x]    //除法
>	divide: function(operandLeft, operandRight) 

- [x]        //校验表达式的合法性
>	isArithmeticExpression: function(expression) 

- [x]   //计算
>	calculate: function(expression)

- [x]   //中缀表达式转后缀表达式
>	infixToPostfixExpression: function(expression) 

```
//demo
var expression='(2+9)*8-24';		
RDIFrameworkExtend.ElementaryArithmeticUtils.infixToPostfixExpression(expression);
```
```
//结果
2 9 + 8 * 24 -
```

- [x]   //中缀表达式转前缀表达式(结果以空格隔开)
>		infixToPrefixExpression: function(expression) 
```
//demo
var expression='(2+9)*8-24';		
RDIFrameworkExtend.ElementaryArithmeticUtils.infixToPrefixExpression(expression);
```
```
//结果
- * + 2 9 8 24
```

- [x]   //解决正负号问题-1转为0-1;+1转为0+1
>	eliminatePositiveOrNegativeSign: function(expression) 

- [x]        //把中缀表达式转为前缀表达式，再计算
>	calculateByPrefixExpression: function(expression) 
```
//demo
var expression='(2+9)*8-24';		
RDIFrameworkExtend.ElementaryArithmeticUtils.calculateByPrefixExpression(expression);
```
```
//结果
["64"]
```

- [x]        //把中缀表达式转为后缀表达式，再计算
>		calculateByPostfixExpression: function(expression) 
```
//demo
var expression='(2+9)*8-24';		
RDIFrameworkExtend.ElementaryArithmeticUtils.calculateByPostfixExpression(expression);
```
```
//结果
["64"]
```

- [x]        //横式计算
>	horizontalCalculation: function(expression) 

```
var expression='1+2*(4-3)/5*[(7-6)/8*9]';		
RDIFrameworkExtend.ElementaryArithmeticUtils.horizontalCalculation(expression);
```
```
//结果
1+2*(4-3)/5*[(7-6)/8*9]=1+2*1/5*[1/8*9]=1+2*1/5*1.125=1+2/5*1.125=1+0.4*1.125=1+0.45=1.45
```

- [x]        //竖式计算
>	verticalCalculation: function(expression)
```
var expression='1+2*(4-3)/5*[(7-6)/8*9]';		
RDIFrameworkExtend.ElementaryArithmeticUtils.verticalCalculation(expression);
```
```
1+2*(4-3)/5*[(7-6)/8*9]
=1+2*1/5*[1/8*9]
=1+2*1/5*1.125
=1+2/5*1.125
=1+0.4*1.125
=1+0.45
=1.45
```
### 6、正则表达式生成工具类；

- [x]  //生成正整数范围的表达式
>	positiveIntegerRange:function(minimum,maximum)

- [x] 排除某些字符串，即不能包含某些字符串.返回值为RegExp对象
>createRegexObjMustExclude:function(input, conditions)

参数说明
 > @param {Object} conditions:里面有多个属性，如下：
 >  @param {String} matcherFlag 匹配标识

>* 0:数字；
>* 1：字母；
>* 2：小写字母；
>* 3:大写字母；
>* 4：特殊字符,指英文状态下的标点符号及括号等；
>* 5:中文;
>* 6:数字和字母；
>* 7：数字和小写字母；
>* 8：数字和大写字母；
>* 9：数字、字母和特殊字符；
>* 10：数字和中文；
>* 11：小写字母和特殊字符；
>* 12：大写字母和特殊字符；
>* 13：字母和特殊字符；
>* 14：小写字母和中文；
>* 15：大写字母和中文；
>* 16：字母和中文；
>* 17：特殊字符、和中文；
>* 18：特殊字符、字母和中文；
>* 19：特殊字符、小写字母和中文；
>* 20：特殊字符、大写字母和中文；
>* 100：所有字符;

> @param {Array} targetStrArr 排除的字符串，数组格式
>  @param {String} length 长度，可为空。1,2表示长度1到2之间；10，表示10个以上字符；5表示长度为5
>  @param {Boolean} ignoreCase 是否忽略大小写

 >条件参数固定格式 conditions={matcherFlag:"0",targetStrArr:[],length:"",ignoreCase:true}
```
var conditions={matcherFlag:"0",targetStrArr:['12','00'],length:"10",ignoreCase:true}
RDIFrameworkExtend.RegexUtils.createRegexObjMustExclude("1234567009",conditions);
```
```
//生成的正则表达式
/^(?!.*(?:12|00))\d{10}$/i
```

- [x]  校验时排除某些字符串，即不能包含某些字符串
> isPatternMustExclude: function(input, conditions)
```
//demo1，10位长度的数字，且不能包含12和00子串
var conditions={matcherFlag:"0",targetStrArr:['12','00'],length:"10",ignoreCase:true}
RDIFrameworkExtend.RegexUtils.isPatternMustExclude("1234567009",conditions);
```
```
//结果
false
```
```
//demo2,10位长度的数字，且不能包含120子串
var conditions={matcherFlag:"0",targetStrArr:['120'],length:"10",ignoreCase:true}
RDIFrameworkExtend.RegexUtils.isPatternMustExclude("1234567009",conditions);
```
```
//结果
true
```

- [x] 必须同时包含某些字符串,返回值为RegExp对象
> createRegexObjMustContain:function()
```
var conditions={matcherFlag:"0",targetStrArr:['120'],length:"10",ignoreCase:true}
RDIFrameworkExtend.RegexUtils.createRegexObjMustContain("1234567009",conditions);
```
```
/^(?=.*120)\d{10}$/i
```

- [x] 校验必须同时包含某些字符串
> isPatternMustContain: function(input, conditions)
```
//demo1
var conditions={matcherFlag:"0",targetStrArr:['120'],length:"10",ignoreCase:true}
RDIFrameworkExtend.RegexUtils.isPatternMustContain("1234567009",conditions);
```
```
false
```
```
//demo2
var conditions={matcherFlag:"0",targetStrArr:['12','00'],length:"10",ignoreCase:true}
RDIFrameworkExtend.RegexUtils.isPatternMustContain("1234567009",conditions);
```
```
true
```
### 7、日期工具
- [x] 获取当前时间
 > getCurrentTime:function()

```
RDIFrameworkExtend.DateUtils.getCurrentTime();
```
```
2017-9-1 16:28:50
```

- [x] 	/*
		 * 比较时间大小
		 * time1>time2 return 1
		 * time1<time2 return -1
		 * time1==time2 return 0
		 */
> compareTime: function(time1, time2)

- [x] 是否闰年
>	isLeapYear: function(year) 

- [x] 获取某个月的天数，从0开始
>	getDaysOfMonth: function(year, month)
>	
>	getDaysOfMonth2: function(year, month)

- [x] 距离现在几天的日期：负数表示今天之前的日期，0表示今天，整数表示未来的日期. 如-1表示昨天的日期，0表示今天，2表示后天
	
>		fromToday: function(days) 

- [x] /**
		 * 日期时间格式化
		 * @param {Object} dateTime 需要格式化的日期时间
		 * @param {String} pattern  格式化的模式，
		 * 如yyyy-MM-dd hh(HH):mm:ss.S a k K E D F w W z Z
		 */
>	formt: function(dateTime, pattern)

```
//demo1
RDIFrameworkExtend.DateUtils.formt(new Date(),'yyyy-MM-dd hh(HH):mm:ss.S a k K E D F w W z Z');
```
```
2017-09-01 04(16):37:25.246 下午 16 4 五 244 0 35 1 GMT +0800
```
```
//demo2
RDIFrameworkExtend.DateUtils.formt(new Date(),'yyyy年MM月dd日  a hh(HH)时mm分ss秒S毫秒 星期E 今年的第D天  这个月的第W周 今年的第w周');
```
```
2017年09月01日  下午 05(17)时07分14秒678毫秒 星期五 今年的第244天  这个月的第1周 今年的第35周
```

- [x] /**
		 * 计算一个日期是当年的第几天
		 * @param {Object} date
		 */
>	dayOfTheYear: function(date)

- [x] //获得时区名和值
> getZoneNameValue: function(dateObj) 

### 8、url工具

- [x] 获取url参数，转为obj
 > urlToObj:function(url)

 ```
 var url="https://www.baidu.com/s?ie=utf-8&f=3&rsv_bp=1&rsv_idx=1&tn=62004195_oem_dg&wd=segmentfault&oq=%25E5%2588%25A4%25E6%2596%25AD%25E6%25B5%258F%25E8%25A7%2588%25E5%2599%25A8%25E7%2589%2588%25E6%259C%25AC%25E6%2598%25AF%25E5%2590%25A6%25E4%25BD%258E%25E4%25BA%258Eie8&rsv_pq=d79dd42400021771&rsv_t=8c28cMqwUPOPwQSHQaUBXyeyoarfbqdxd2zF9iM3QeBHAlBhE8pg56EnR7OU4tJeeo2yyx9A&rqlang=cn&rsv_enter=1&inputT=3251&rsv_sug3=70&rsv_sug1=62&rsv_sug7=100&rsv_sug2=1&prefixsug=sef&rsp=1&rsv_sug4=3251";
 var result=RDIFrameworkExtend.UrlUtils.urlToObj(url);
 ```
 - [x] obj属性值转为url参数
 > objToUrl:function(baseUrl,obj)

 - [x] url参数转obj,若一个字段有多个值的话,返回数组
 > parseQueryString: function(url) 

---