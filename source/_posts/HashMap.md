---
title: HashMap方法集详解
---

## computeIfAbsent 方法

> 描述：computeIfAbsent 用于获取key对应的value，如果key不存在，则将生成的值存入map中，并返回

```java 
public class MapTest {
    public static void main(String[] args) {
        Map<String,String> map = new HashMap<>();
        map.put("key1","张三");
        // 如果key存在，则返回key对应的value，如果不存在，则将生成的值存入map中，并返回
        System.out.println(map.computeIfAbsent("key1", k -> getNum()));
        System.out.println(map.computeIfAbsent("key2", k -> getNum()));
    }

    private static String getNum(){
        return "函数生成数据";
    }
}
```
```text
输出:
张三
函数生成数据
```

## putIfAbsent 方法

> 描述：putIfAbsent 用于获取key对应的value，如果key不存在，则将存固定的值存入map中，并返回key上一个存值

```java 
public class MapTest {
    public static void main(String[] args) {
        Map<String,String> map = new HashMap<>();
        map.put("key1","张三");
        System.out.println(map.putIfAbsent("key1", "存固定的值"));
        System.out.println(map.putIfAbsent("key2", "value"));//存入固定值,返回上一个存值
        System.out.println(map.get("key2"));
    }
}
```
```text
输出:
张三
null
value
```