---
title: jdk21新特性
---

## 增强的 switch 表达式

> 描述：switch 现在可以用作表达式，支持返回值，并支持 case 的合并及模式匹配

```java 
public class Main {
    public static void main(String[] args) {
        String day = "MONDAY";
        String result = switch (day) {
            case "MONDAY", "FRIDAY" -> "Workday";
            case "SATURDAY", "SUNDAY" -> "Weekend";
            default -> throw new IllegalArgumentException("Unknown day");
        };
        System.out.println(result);  // 输出：Workday
    }
}
```

## 虚拟线程（Virtual Threads）

> 虚拟线程是轻量级线程，由 JDK 管理的，可以创建大量线程而不会产生过多的资源开销

```java
public class Main {
    public static void main(String[] args) throws InterruptedException {
        Thread.startVirtualThread(() -> {
            System.out.println("Hello from virtual thread");
        }).join();
    }
}
```

## 流（Stream API）增强

> 新方法：takeWhile、dropWhile、iterate 流操作新增了 takeWhile 和 dropWhile，用于基于条件筛选流元素，iterate 可以创建无限流

```java
public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5, 6);
        numbers.stream().takeWhile(n -> n < 4).forEach(System.out::println); // 输出 1, 2, 3
    }
}
```

## 集合 API 增强

> List.of、Set.of、Map.of 静态工厂方法 用于创建不可变的集合对象，简化了集合初始化的过程

```java
public class Main {
    public static void main(String[] args) {
        List<String> list = List.of("a", "b", "c");
        Set<String> set = Set.of("a", "b", "c");
        Map<String, Integer> map = Map.of("a", 1, "b", 2);
    }
}
```

> copyOf 方法用于创建现有集合的不可变副本

```java
public class Main {
    public static void main(String[] args) {
        List<String> list = List.of("a", "b");
        List<String> copyList = List.copyOf(list); // 创建不可变副本
    }
}
```

## 新日期和时间 API

> JDK 8 引入了 java.time API，JDK 21 中此 API 经过改进，支持更多的日期和时间操作

```java
public class Main {
    public static void main(String[] args) {
        LocalDate date = LocalDate.now();
        LocalTime time = LocalTime.now();
        LocalDateTime dateTime = LocalDateTime.of(date, time);
    }
}
```

> 其他增强特性

```java
public class Main {
    public static void main(String[] args) {
        String json = """
                {
                    "name": "John",
                    "age": 30
                }
                """;
    }
}
```
> Var 局部变量类型推断

```java
public class Main {
    public static void main(String[] args) {
        var list = List.of("a", "b", "c");
        for (var item : list) {
            System.out.println(item);
        }
    }
}
```