---
title: RAML
grammar_cjkRuby: true
---

### 前言
介绍和语法教程见附件pdf即可。
>1、[raml0.8API文档][13] 
2、[raml1.0API文档][14]
3、[语法规范][15]
### API-manager
在线api设计器：https://anypoint.mulesoft.com/home/#/  （账户：liaodd 密码：1QAZ2wsx 写了一个例子）
打开api-manager，点击Add new API，填写相应信息创建
![enter description here][1]
![enter description here][2]
点击编辑，默认进入编辑页面会有之前填写的基本信息
![enter description here][3]
然后就可以进行相应的接口编写，功能很强大所以宝宝还没有参透，只使用了最最基本的东西，并且try it一直网关超时不知道如何能像swagger那样在线调用还没研究出来
![enter description here][4]
写完接口后新建portal,如果已有写到的方法会自动创建
![enter description here][5]
点击预览按钮，之前写的方法即会像在线文档一下显示
![enter description here][6]
![enter description here][7]
### java解析器使用
https://github.com/raml-org/raml-java-parser java解析器
#### **解析器的构建**
将源代码clone下来，因为工程有依赖所以按照readme执行 ==mvn clean package -P jar-with-dependencies==在clone目录\target目录下即出现jar包
![enter description here][8]
#### **API校验**
1、通过==java -jar raml-parser-{version}.jar raml-file== 可以校验所写的api是否格式是否正确
![enter description here][9]
2、通过代码==List<ValidationResult> results = RamlValidationService.createDefault().validate(ramlLocation);== 校验，如果格式正确返回空数组，如果有问题则返回错信息，如修改URI为错误路径后：
![enter description here][10]
#### **解析/反解析**
通过==Raml raml = new RamlDocumentBuilder().build("D:/api.raml");== 解析raml文件获得raml对象然后可以通过相应方法获取数据
通过Emitter类可以修改raml文件==RamlEmitter emitter = new RamlEmitter();String dumpFromRaml = emitter.dump(raml);==

### 个人感觉
感觉还是swagger顺手
附gongzf的两篇swagger文章
[dubbox swagger 学习][11]
[dubbox项目集成swagger][12]






 


  [1]: ./images/1465353432947.jpg "1465353432947.jpg"
  [2]: ./images/1465376780952.jpg "1465376780952.jpg"
  [3]: ./images/1465374916711.jpg "1465374916711.jpg"
  [4]: ./images/1465375418928.jpg "1465375418928.jpg"
  [5]: ./images/1465376955656.jpg "1465376955656.jpg"
  [6]: ./images/1465377096642.jpg "1465377096642.jpg"
  [7]: ./images/1465377073526.jpg "1465377073526.jpg"
  [8]: ./images/1465350669420.jpg "1465350669420.jpg"
  [9]: ./images/1465350847269.jpg "1465350847269.jpg"
  [10]: ./images/1465351132424.jpg "1465351132424.jpg"
  [11]: http://10.1.2.218/kb/pages/viewpage.action?pageId=8946711
  [12]: http://10.1.2.218/kb/pages/viewpage.action?pageId=9732568
  [13]: https://github.com/raml-org/raml-spec/blob/master/versions/raml-08/raml-08.md
  [14]: https://github.com/raml-org/raml-spec/blob/master/versions/raml-10/raml-10.md
  [15]: http://raml.org/developers/raml-100-tutorial