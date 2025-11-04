# Chapter 2 — Hashing Out a Plan

> The coordinates Satoshi gave you don't disappoint, unfortunately: it's a warehouse, and a scary, deserted one to boot.  
> You circle the warehouse in your Budgetcopter no less than three times. Yeah, sigh, you're probably gonna have to go in there. Your Budgetcopter's Budget Heat Detector detects nothing but darkness. If someone knows that this place exists, it's been a long time since they visited it in anything but their memory.

中本聪给你的坐标：真没让你失望 —— 但不是好的那种。  
那是个仓库，而且令人发毛、空旷、荒凉。

你开着 Budgetcopter 绕着仓库飞了至少三圈。  
唉，看起来最终还是得进去。  
机载的低配热像仪只扫到一片死寂。  
如果有人知道这地方，那也是很久以前的事了。

---

### Intro

> —HOLOCAT: “Boy, what a dump. This place had better have some e-anchovies stored somewhere. I'd even settle for some CyberKibble.."

Holocat：这地方也太破了吧……最好里面至少还有点 e-凤尾鱼。要不 CyberKibble 也行。

你降落、稳好身形、开始找入口。  
那里 —— 有个破窗够用了。  
你拿起块砖把剩下那点碎玻璃敲掉，翻身进去。

仓库里赫然摆满数千台蒙着灰、但保存完整的老式比特币矿机。

> —HOLOCAT: “This isn't a warehouse; this is a museum. I think these are old Vanderpoole family mining devices. In bitcoin's early days, miners would use general purpose computers to mine bitcoin. But after a few years, miners realized they could use machines with a special chip called an Application-Specific Integrated Circuit, or ASIC for short. These chips do only one thing: mine bitcoin. Their narrow focus increases their efficiency and allows miners to spend less energy on mining, giving them an edge. Can you believe that people mined with their laptops at one point?"

Holocat：这不是仓库，是博物馆。  
这些应该是范德普尔家族旧矿机。  
早期的比特币，是用普通电脑挖的。  
后来大家发现可以专做一片芯片 —— ASIC  
Application-Specific Integrated Circuit  
只干一件事：挖比特币。不通用，但效率高。

你能想象吗？以前有人直接用笔记本挖矿……

这也解释了为什么这仓库里堆了一整代矿机。

---

### Hashing out a plan

角落里，有个昏暗但仍亮着的显示器，上面贴着一张纸条：  
“Turn them on, stupid.”  
（开机啊笨蛋）

> —HOLOCAT: “How rude. Wow; a mechanical keyboard. I've heard about these things. Supposedly, they were so loud that they cost users their hearing, and were banned.”

Holocat：好没礼貌。哇机械键盘。听说过去这玩意巨吵，吵到会搞坏人听力，后来被禁…

Holocat 跳上键盘，乱走几步，键盘打出随机字符：
QX23Y6VGECTUKSNIEUTUB[P[pihof
1c31d1d9fb848a505fc0cdbea848ff1bdd46a9ed4d639d413d3a93035194eedf

显示器提示：  
`INCORRECT HASH. TRY AGAIN.`

当然这是错误的。  
Holocat 就是一只嚣张的 hologram 猫。

---

于是问题来了：

> What happens if you type something different?

如果换别的输入，会怎样？

---

然后：

> Did you notice anything special about the hashes?  
> • hashes are unique  
> • one-way  
> • deterministic  
> SHA-256

你注意到了吗？

- 哈希像指纹一样：几乎唯一  
- 哈希是单向 → 无法反推  
- 同一输入 → 永远同一输出

这里用的是 SHA-256  
（比特币最核心的哈希函数）

---

接下来：

> Find a hash that starts with a zero (“0”). Keep typing different things...

下面就是 PoW 的核心味道。

要找到一个结果以“0”开头的哈希  
输入不停变  
循环尝试  
直到成功。

这就是挖矿的缩影。

---

**( END of Chapter 2 narrative section )**