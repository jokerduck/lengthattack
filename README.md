# lengthattack

#实验名称

SM3—rho-attack

#实验简介

implement the Rho method of reduced SM3

#姓名

王晖

202100141110

githubID：jokerduck

#实验思路

本次实验针对SM3进行长度扩展攻击，攻击过程大体如下：

1、对任意消息r1，首先对其进行填充，得到 m=r1||padding；

2、调用SM3计算哈希值即 h1=SM3(m,IV)；

3、自选r2作为进行攻击的消息，计算 h2=SM3(m||r2,IV)即h2=SM3(r1||padding||r2,IV)；

4、计算 h3=SM3(r2,iv)，其中iv=h1即先前消息的哈希值；

5、比较h2与h3是否相同，若相同，则攻击成功。

![image](https://github.com/jokerduck/lengthattack/assets/130890730/3d006dc0-d944-4931-85dc-ec3380338c7e)
