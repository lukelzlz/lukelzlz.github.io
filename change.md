# 改进方案

捕食。一次获取10氨基酸10葡萄糖，开始只能手动按按钮，升级可以增加获取，一定级别之后数量不再提升但是可以改为获取 淀粉/脂肪/糖原 和 蛋白质，后者的获取量会一直随着等级提高而提高。间隔若干级之后会锁住，需要升级细胞膜至对应等级后才能继续升级。解锁自动化之后间隔若干秒捕食一次，并增加一个升级按钮，减少两次捕食之间的间隔。升级均需要结构蛋白质。
吸气。细胞膜二级解锁。吸可以获取10份O2，可以设置更改哪种气体（比如H2？）但是呼吸量由等级决定。间隔若干级之后会锁住，需要升级细胞膜至对应等级后才能继续升级。升级需要结构蛋白质。自动化同上。
排泄。按下之后可以选择排出什么物质，最短5分钟一次，一次最多20，升级后可增加数量，减少时间。升级需要结构蛋白质。间隔若干级之后会锁住，需要升级细胞膜至对应等级后才能继续升级。
玩家一开始有0级细胞核，1级细胞膜，1个核糖体，以及细胞质（不分等级）

## 细胞质

可以进行无氧呼吸，磷酸戊糖途径或者合成RNA。产量无法升级。自动化同上，但是升级自动化需要酶
无氧呼吸：第一行：葡萄糖-1，丙酮酸+2，能量+2，2NAD->2NADH（NAD开始赠送20个，前期无法通过随机事件以外的方式获取）
第二行：1丙酮酸->1乳酸，NADH->NAD
第三行：葡萄糖-1，乳酸+2，能量+2
磷酸戊糖途径：葡萄糖-1，CO2+6，6NADP->6NADPH（新手教程应该指出，NADPH用来为细胞其他地方提供H，比如合成DNA和叶绿体中，而NADH用来提供能量）
RNA/DNA合成：开始：葡萄糖-1，氨基酸-5，结束：有氧呼吸中间体+3，CO2+1，RNA/DNA+1。（开始后再过若干秒结束，该项目可以升级缩短持续时间，初始时合成时间特别长，升级消耗酶和DNA）

## 核糖体

无法升级产量，但是可以增加数量。需要RNA获取新的。自动化一开始就可以，依然需要升级减少时间。升级需要RNA。
可设置多种设置，对于不同核糖体有不一样的操作。
第一种：若干氨基酸->1结构蛋白质，能量-若干
第二种：把结构蛋白质换成酶

## 细胞膜

无功能。消耗结构蛋白质升级。二级后会触发随机事件：获得线粒体，三级后触发事件：获得叶绿体

## 线粒体

无法升级产量，但是可以增加数量。需要结构蛋白质和酶获取新的线粒体。自动化需要分别解锁，依然需要升级减少时间。升级需要酶。自动化全部解锁后之后可以解锁自调整产量使产量最大化功能。可设置多种设置，对于不同线粒体有不一样操作。
每个线粒体内存在单独的存储空间
线粒体-传输：极短时间内运输。可单独升级单次运输效率
有氧呼吸-初始化：细胞质内丙酮酸-1，线粒体内乙酰CoA+1，线粒体内1NAD->1NADH
有氧呼吸-主体：开始时：草酰乙酸-1，乙酰CoA-1。结束时：草酰乙酸+1，CO2+2，4NAD->4NADH，能量+1  （开始后再过若干秒结束，该项目可以升级缩短持续时间，升级消耗酶）
有氧呼吸-部分：开始时：有氧呼吸中间体-1。结束时：草酰乙酸+1，CO2+2，3NAD->3NADH，能量+1（开始后再过若干秒结束，该项目可以升级缩短持续时间，升级消耗酶）
有氧呼吸-调整：乙酰CoA-1，草酰乙酸+1，能量-2
有氧呼吸-产能：5NADH->5NAD，O2-5，能量+10

## 叶绿体

正在补课中。。。。。。

## 细胞核

细胞核内能够解锁各种功能，均需要DNA
之后可以解锁自动建造。