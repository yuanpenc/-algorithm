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
### 最长回文字串

### 背包问题
```
package knapsack;

public class knapsack {
	
	private int item=6;
	private int weight=21;

	
	int[][] bag=new int[item][weight];
	private int[] itemList= {0,3,4,5,8,10};
	private int[] weightList= {0,2,3,4,5,9};
	

	
	public void solution() {
		for (int i=1;i<item;i++) {
			for (int w=1;w<weight;w++) {
				if(weightList[i]>w) {
					bag[i][w]=bag[i-1][w];
				}
				else {
					int value1=bag[i-1][w];
					int value2=bag[i-1][w-weightList[i]]+itemList[i];
					
					bag[i][w]=Math.max(value1, value2);
				}
			}
		}
		
	
	}

	public static void main(String[] args) {
		knapsack case1 =new knapsack();
		case1.solution();
		for(int i=0;i<6;i++) {
			for (int j=0;j<21;j++) {
				System.out.print(case1.bag[i][j]);
			}
			System.out.println();
		}
		
	}
}

################################################
result:
000000000000000000000
003333333333333333333
003447777777777777777
003457899121212121212121212121212
00345881112131516171720202020202020
00345881112131516171720202122232526
################################################
```

