# Java编码规范

## 1.统一注释风格

### 文件头和版权信息

+ 文件头部模板

在IDEA中选择 **File** -> **Settings** -> **File and Code Templates** 选择Includes标签的FileHeader文件中加入如下代码

```java

/**
 * Zentech-Inc
 * Copyright (C) ${YEAR} All Rights Reserved.
 */
```
+ 类模板

![image](/uploads/aa88823244f7915ba61061ed3a8afbb2/image.png)

```java

#parse("File Header.java")
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end

/**
 *
 * @author ${USER}
 * @version \$Id ${NAME}.java, v 0.1 ${YEAR}-${MONTH}-${DAY} ${TIME} ${USER} Exp $$
 */
public class ${NAME} {
}

```

+ 接口模板

```java

#parse("File Header.java")
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end

/**
 *
 * @author ${USER}
 * @version \$Id ${NAME}.java, v 0.1 ${YEAR}-${MONTH}-${DAY} ${TIME} ${USER} Exp $$
 */
public interface ${NAME} {
}


```

+ 枚举模板

```java
#parse("File Header.java")
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end

/**
 *
 *
 * @author ${USER}
 * @version \$Id ${NAME}.java, v 0.1 ${YEAR}-${MONTH}-${DAY} ${TIME} ${USER} Exp $$
 */
public enum ${NAME} {
}

```

# C#编码规范

## 1. 统一注释风格

### 文件头和版权信息

需要修改VS新建文件模板的内容，目录如下：C:\Program Files (x86)\Microsoft Visual Studio 14.0\Common7\IDE\ItemTemplates\CSharp\Code\2052\Class，找到之后直接用下面的代码覆盖文件内容即可，如果提示没有权限的话需要用管理权限打开记事本。

 + 类的模板：

```csharp
/**
* Zentech-Inc
* Copyright (C) $year$ All Rights Reserved.
*/
namespace $rootnamespace$
{
	/**
     * 
     * $safeitemrootname$.cs Version 1.0 Create By $username$ On $time$
     */
    public class $safeitemrootname$
    {
    }
}
```
 + 接口的模板：

```csharp
/**
* Zentech-Inc
* Copyright (C) $year$ All Rights Reserved.
*/
namespace $rootnamespace$
{
	/**
     * 
     * $safeitemrootname$.cs Version 1.0 Create By $username$ On $time$
     */
    public interface $safeitemrootname$
    {
    }
}
```
### 统一注释

所有方法和公有属性的注释都用xml doc的方式写，所有变量和私有字段的注释都用传统双斜杠，**注释不能写在代码之后，必须新起一行，写在代码上面一行**，下面是一个完整的例子：

```csharp
/**
* Zentech-Inc
* Copyright (C) 2016 All Rights Reserved.
*/

using System;

namespace Zentech.Coupon.Api
{
    /**
     * This is a Class
     * Class3.cs Version 1.0 Create By wujn On 2016/5/15 19:38:39
     */
    public class AClass
    {
        // this is a field
        private string hello;
        /// <summary>
        /// This is a property
        /// </summary>
        public string Hello { get; set; }
        /// <summary>
        /// main method
        /// </summary>
        /// <param name="args">console parameters</param>
        public static void Main(string[] args)
        {
            //用户名
            var username = "wujn";
            //密码
            var pwd = "password";
            //print
            Console.WriteLine(username + pwd);
        }
    }
}

```
### 统一命名规则
这个可以借用ReSharper的功能来帮忙，规范就不做过多描述了，内容如下。

![image](/uploads/c3c0854f7540d71652535cdd5a4bd081/image.png)

[zentech.resharper-settings.zip](/uploads/3cf8cdecedf70887aae09fca4f9bb5e6/zentech.resharper-settings.zip) 是ReSharper的配置，导入到自己的VS中之后(**导入的时候需要解压出来**)，如果没有按规范命名，VS会标记出来，需要自己修复。如下图

![image](/uploads/4803b29f57515f78f6df8e7a22ed9d08/image.png)

导入方法：

![image](/uploads/41a55edc3e385b4317600a9329f62756/image.png)

![image](/uploads/f3f7f01940bdfdb56eccc374e0fe6391/image.png)
