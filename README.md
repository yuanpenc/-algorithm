# 面试算法总结

## HashMap
```
HashMap<Character,Integer> count=new HashMap<,>();
count.put(character,character.getOrDefault((charater,0)+1));

############################################################

############################################################

HashMap h=new HashMap();
//增加或修改一组键值对
h.put("key","value");
//查找一组键值对
h.get("key");
//删除一组键值对
h.remove("key");

//遍历HashMap

HashMap h=new HashMap();
for(int i=0;i<5;i++){
h.put("a"+i,i);
}

for(Object key:h.keySet()){
System.out.println("key:"+key+"value:"+h.get(key));
}

//第二种遍历HashMap的方法

HashMap<String,String> h=new HashMap<String, String>();
h.put("key","value");
for(Map.Entry<String,String> e:h.entrySet()){
String key=e.getKey();
String value=e.getValue();
}


```

## ArrayList
```
ArrayList list=new ArrayList();
//增加一个值
list.add("aaa");
//修改一个值
list.set(0,"asd");
//查找一个值
System.out.println(list.get(0));
//删除一个值
list.remove(0);
//遍历
for(int i=0;i<list.size();i++){
Object j=(String)list.get(i);
}
```





## 字符串（string）

## Dynamic Programming
### [线性规划各种模型](https://blog.csdn.net/u013309870/article/details/75193592?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)



