---
title: java中的大数
---

## BigDecimal 适用于任意精度的浮点数运算

> 1、add(BigDecimal val): 两个大浮点数相加

```java
import java.math.BigDecimal;

public class BigDecimalTest {
    public static void main(String[] args) {
        BigDecimal bigDecimal = new BigDecimal("50000000");
        BigDecimal bigDecimal1 = new BigDecimal("30000000");
        bigDecimal = bigDecimal.add(bigDecimal1);
        System.out.println("bigDecimal:"+bigDecimal);
        // 结果：bigDecimal:80000000
    }
} 
```

> subtract(BigDecimal val): 两个大浮点数相减

```java
import java.math.BigDecimal;

public class BigDecimalTest {
    public static void main(String[] args) {
        BigDecimal bigDecimal = new BigDecimal("50000000");
        BigDecimal bigDecimal1 = new BigDecimal("30000000");
        bigDecimal = bigDecimal.subtract(bigDecimal1);
        System.out.println("bigDecimal:"+bigDecimal);
        // 结果：bigDecimal:20000000
    }
}

```

> multiply(BigDecimal val): 两个大浮点数相乘

```java
import java.math.BigDecimal;

public class BigDecimalTest {
    public static void main(String[] args) {
        BigDecimal bigDecimal = new BigDecimal("50000000");
        BigDecimal bigDecimal1 = new BigDecimal("30000000");
        bigDecimal = bigDecimal.multiply(bigDecimal1);
        System.out.println("bigDecimal:"+bigDecimal);
        // 结果：bigDecimal:150000000000000000
    }
}

```

> divide(BigDecimal val, RoundingMode roundingMode): 两个大浮点数相除，结果可以指定舍入模式

```java
import java.math.BigDecimal;

public class BigDecimalTest {
    public static void main(String[] args) {
        BigDecimal bigDecimal = new BigDecimal("50000000");
        BigDecimal bigDecimal1 = new BigDecimal("30000000");
        bigDecimal = bigDecimal.divide(bigDecimal1, BigDecimal.ROUND_HALF_UP);
        System.out.println("bigDecimal:"+bigDecimal);
        // 结果：bigDecimal:1.666666666666666666666666666666666666666666666666666666666666666666
    }
}
```

## BigInteger: 适用于任意精度的整数运算

> 1、add(BigInteger val): 两个大浮点数相加

```java
import java.math.BigInteger;

public class BigIntegerTest {
    public static void main(String[] args) {
        BigInteger BigInteger = new BigInteger("50000000");
        BigInteger BigInteger1 = new BigInteger("30000000");
        BigInteger = BigInteger.add(BigInteger1);
        System.out.println("BigInteger:"+BigInteger);
        // 结果：BigInteger:80000000
    }
} 
```

> subtract(BigInteger val): 两个大浮点数相减

```java
import java.math.BigInteger;

public class BigIntegerTest {
    public static void main(String[] args) {
        BigInteger BigInteger = new BigInteger("50000000");
        BigInteger BigInteger1 = new BigInteger("30000000");
        BigInteger = BigInteger.subtract(BigInteger1);
        System.out.println("BigInteger:"+BigInteger);
        // 结果：BigInteger:20000000
    }
}

```

> multiply(BigInteger val): 两个大浮点数相乘

```java
import java.math.BigInteger;

public class BigIntegerTest {
    public static void main(String[] args) {
        BigInteger BigInteger = new BigInteger("50000000");
        BigInteger BigInteger1 = new BigInteger("30000000");
        BigInteger = BigInteger.multiply(BigInteger1);
        System.out.println("BigInteger:"+BigInteger);
        // 结果：BigInteger:150000000000000000
    }
}

```

> divide(BigInteger val, RoundingMode roundingMode): 两个大浮点数相除，结果可以指定舍入模式

```java
import java.math.BigInteger;

public class BigIntegerTest {
    public static void main(String[] args) {
        BigInteger BigInteger = new BigInteger("50000000");
        BigInteger BigInteger1 = new BigInteger("30000000");
        BigInteger = BigInteger.divide(BigInteger1);
        System.out.println("BigInteger:"+BigInteger);
        // 结果：BigInteger:1
    }
}
```