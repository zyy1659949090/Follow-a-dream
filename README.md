# Follow-a-dream

Follow a dream

Problem Description

每个人的童年都可能梦想过自己成为一个英雄，尤其是喜欢武侠的男生，Yifenfei也不例外
	童年的他常常梦想自己能成为一个绝世英雄，手拿一把灿灿发亮的宝剑，手挽一位长发飘逸的秀丽气质MM ^_^ ，散步于清幽的泉边小道，微风吹过，飘落两片枫叶。。。。。。
  
	正由于成天陶醉于这种脱世的意境之中，导致此人老大不小依旧形单影只，每天只能在人潮中孤单上路。。。。。。
	现在就让我们为这个可怜的人创造一个机会，权当假设yifenfei现在已经捕获一位MM的芳心，但该MM被邪恶并且极其可恶的大魔头（AC女之杀手 lemon）抓走。为了正义，为了MM，燃烧吧。。。。。。
  
	好了，现在就正式开始我们的行程，接下来将有6关等待着yifenfei,让我们帮助他战胜邪恶的lemon大魔王吧。
	来到大魔王居住的千年古墓前，呈现在yifenfei眼前的是墓碑上神秘的字符，经过仔细研究，发现原来这是开启古墓入口的方法。
	墓碑上有2行字符串，其中第一个串的长度为偶数，现在要求把第2个串插入到第一个串的正中央，如此便能开启墓碑进入墓中。
  
Input

输入数据首先给出一个整数n，表示测试数据的组数。

然后是n组数据，每组数据2行，每行一个字符串，长度大于0，小于50，并且第一个串的长度必为偶数。

Output

请为每组数据输出一个能开启古墓的字符串，每组输出占一行。

Sample Input

2 HDCM UA Aw CFlo

Sample Output

HDUACM ACFlow

代码：

#include<stdio.h>

#include<string.h>

main()

{

    int n,l1,l2,i,j;
    
    char a[100],b[50];
    
    scanf("%d",&n);
    
    while(n--)
    
    {
    
    
        for(i=0;i<50;i++)
        
        {a[i]=0;b[i]=0;}
        
        j=0;
        
        scanf("%s %s",a,b);
        
        l1=strlen(a);
        
        l2=strlen(b);
        
        for(i=l1/2;i<l1;i++)
        
            a[i+l2]=a[i];
            
        for(i=l1/2;i<l1/2+l2;i++)
        
            a[i]=b[j++];
            
            puts(a);
            
    }
    
}
