# Chapter 3 — The 51% Attack

> You enter the address of a block explorer and see that blocks are back to ten minute intervals. Somehow, Holocat sleeps through the noise from all the ASICs.  
> Cats. What can you do?

你打开区块浏览器，发现区块间隔又回到 10 分钟了。  
Holocat 居然在 ASIC 噪音旁边睡得死死的。  
猫嘛。还能怎样。

然而，有哪里不对劲：

> The blocks are empty, and transactions aren't processing.

区块是空的。  
交易没有被处理。

你是不是做错了？  
还是巧合？  
下一个窗口弹出来，把 Holocat 震醒。

> It's not a coincidence.

这不是巧合。

> —SATOSHI NAKAMOTO: “Hey, you! Yeah, you! Remember me? Bitcoin is being hit with a 51% attack right now! After you brought those mining devices online, Vanderpoole turned BitRey's ASICs back on and is mining empty blocks. The problem is it's not just his machines. He used a backdoor on the standard ASIC firmware to infect existing miners with a virus that prevents them from mining anything but empty blocks. He's trying to hold the bitcoin ecosystem hostage and force people to support the idea of increasing bitcoin's supply. Do something, dingdong!”

中本聪：  
“嘿！你！还记得我吗？比特币现在正遭 51% 攻击！  
你把那些老矿机启动后，Vanderpoole 把 BitRey 的 ASIC 全部重新上线，并开始只挖空块。  
不仅如此 —— 他在标准 ASIC 固件里留过后门，感染了其他矿机，给它们下病毒，让它们只能挖空块。  
他想通过挟持网络，让人支持增发比特币。  
快做点什么，笨蛋！”

旧显示器呛出一团灰，然后吐出一份“spreadsheet” ——  
里面是全球最大矿工的联络方式，还有病毒补丁。  
越快发出去，越快恢复算力。

Holocat：  
“我们还有活要干。  
准确说 —— 你有。  
我去穿墙吓老鼠去了。”

---

你决定先自己试试 —— 不等其他矿工响应。  
看看能不能单挑 BitRey。

> How do you think this will go?

模拟开始。  
你开始与 BitRey 赛跑挖块。

结果很糟。  
算力完全不够。

---

于是你等待别人加入。  
全世界被你 ping 的矿机 —— 在一台台被修复。

当更多矿工加入你这边后，算力看起来已经接近可以抵抗 BitRey。

但问题又来了：  
大家还是没找到块。

奇怪。

---

### extraNonce 的秘密

> Something is not quite right yet.  
> Hashrate Hoppers, the one with the most hash power, is finding all your blocks but others find nothing.

有个大算力矿工能找到块  
其他都找不到

为什么？

因为大家在做重复工作。

每个矿工都在试**同样**的 nonce 区间  
浪费算力。

---

于是你决定切换策略：

在打包区块时  
在 coinbase 里放一个唯一参数 —— `extraNonce`

> For the Stratum mining pool protocol (not bitcoin protocol), the coinbase transaction also has something called the “extra nonce”.

Stratum（矿池通信协议，不是比特币协议）  
会把 extraNonce 分成两部分：

- extranonce1（矿池分配用，标识矿工）
- extranonce2（矿机自己递增用，做工作量分片）

优势：

- pool participants 不会做重复工作
- pool 可以保持交易列表不变，只递增 extranonce2
- pool 可按 extranonce1 识别矿工贡献

于是，每个矿工：

- 循环 nonce
- 找不到 → 改 extranonce2 再循环
- 再找不到 → 继续

这样全网算力才真正“并行”。

---

**( END of Chapter 3 narrative section )**