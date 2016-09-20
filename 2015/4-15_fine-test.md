# 1. Java代码中的命名
## 1.1 类的命名
在Java中，类的命名，每个单词的第一个字母大写，这种写法又称为Pascal大小写。例如：

      public class InputStream implements Closeable {
      }

## 1.2 成员变量和方法的命名
在Java中，成员变量的命名方式是，第一个单词首字母小写，其余单词首字母大写。例如：

      public class PrintWriter extends Writer {
            protected Writer out;
      }

注意，成员变量的名字不要使用m_前缀，m_前缀命名是一种不推荐的丑陋的命名方式。

## 1.3 常量的命名
有一种约定俗称的做法是：常量大写。

      public class InputStream {
            private static final int MAX_SKIP_BUFFER_SIZE = 2048;
      }

在这例子中，常量的单词是全部大写，单词之间使用下划线区分。

      public class MyService {
            public static final Logger LOG = LogFactory.getLog(MyService.class);
      }

一般类中的logger对象都应该是static final修饰的，属于常量，建议使用大写！

if是代码中最常见的控制语句了。编写if语句需要注意一些事情，使得代码更容易维护。

# 2 每个条件一行
每个条件一行的做法，在于使得代码更好调试。

### 2.1 普通写法

      if (x.isFull() || y.isFull()) {
            // ...
      }

这种写法很常见，很多人都是这么做的，但是这样做有一些坏处：
* 1) 不方便调试，需要调试时，由于设置断点是针对整行的，无法对单个条件设置断点，也对逐行调试不友好。
* 2) 发生异常时，无法通过行号来知道哪个条件出错。上面的例子，如果x或者y是null，产生NullPointerException，无法判断是哪一个条件产生的。

### 2.2 更容易维护和调试的写法

      if (x.isFull() //
            || y.isFull()) {
            // ...
      }

代码中每个逻辑段落之间应该用一个空行分隔开。

比如JDK类中的这个方法：java.math.BigInteger.BigInteger(byte[])

    private BigInteger(int[] val) {
        if (val.length == 0)
            throw new NumberFormatException("Zero length BigInteger");

        if (val[0] < 0) {
            mag = makePositive(val);
            signum = -1;
        } else {
            mag = trustedStripLeadingZeroInts(val);
            signum = (mag.length == 0 ? 0 : 1);
        }
    }

在这个例子中，第一个段落为输入参数校验，和后面逻辑处理的代码之间有一空白行。
