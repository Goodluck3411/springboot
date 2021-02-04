

# ***springboot入门项目***

```md
开发环境：
	这里我们使用：
		SDK：1.8
		JDK:8
		mvean:3.3.5
```

# 	**idea-->创建springboot项目**

![image-20210204115959805](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20210204115959805.png)	

注：这是IDEA集成快速开发的步骤

![image-20210204120223871](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20210204120223871.png)	

注：在这里我们可以选择配置。

## 接下来引入一些依赖。因为是开始项目，我们选择web。

```java
总体项目的结构
```

![image-20210204120439966](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20210204120439966.png)	

```java
这个是HelloController类，
package com.sun.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;
//自动装配！原理！
@RestController
public class HelloController {
    //接口：http://localhost:8080/hello
    @RequestMapping("/hello")
    public String hello(){
        //调用业务，接受前端参数
        return "Hello world";
    }
}
```

```java
package com.sun;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
//程序的主入口
@SpringBootApplication
public class SpringbootApplication {

    public static void main(String[] args) {

        SpringApplication.run(SpringbootApplication.class, args);
    }

}
```

### 3.测试

```makefile
test
```

![image-20210204120637046](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20210204120637046.png)`