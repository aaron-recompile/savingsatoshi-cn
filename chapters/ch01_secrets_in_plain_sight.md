# Chapter 1 — Secrets in Plain Sight

> The year is 2139. The last bitcoin is two weeks from being mined. For months, a clock has ticked down in Satoshi Square. Up until this point, every block has had some kind of bitcoin reward, a subsidy. This is the only way new bitcoins come into existence but soon, it's about to change. After over one hundred years, the issuance schedule for bitcoin is coming to an end. The world awaits for the last block with a subsidy to be mined. It's a historical event. The end of an era.  
> Suddenly, the network grinds to a halt.

2139 年，比特币还剩下最后两周就要被挖完。中本聪广场的倒计时钟已经数月滴答作响。过去这一百多年里，每个区块里都有补贴奖励，这是新比特币唯一的发行方式。但现在，这即将终结。全世界都在等待“最后一个含补贴的区块”。这是一个时代的终点。  
突然，比特币网络停了。

> Moments later, your Hover Screen activates.

片刻后，你的悬浮屏亮起。

> —Deborah Chunk: “Thomas Vanderpoole. As the well-dressed CEO of BitRey, you run, by far, the largest bitcoin mining pool in the world. You also manufacture bitcoin mining machines. What is happening? Is bitcoin dying?”  
> —Vanderpoole: “Let's start from the top. Yes, I am, Deborah, and yes, I do. The Vanderpooles—my well-dressed daddy and his well-dressed daddy before him—have been mining since block 21,000. That's why I can confidently say that miners across the world are causing these delays by turning off their machines. This is a protest. No one wants bitcoin to stop being issued at 21 million. Miners cannot survive on fees alone.”

德博拉：“Thomas Vanderpoole，作为 BitRey 的 CEO，你们是全球最大的矿池供应商，同时也制造矿机。发生什么了？比特币要死了吗？”  
范德普尔：“先从头说吧。是的我是 CEO。我们家从 21,000 区块就开始挖。全球矿工现在关闭机器是在抗议 —— 没人愿意让发行停在 2100 万。靠手续费矿工活不下去。”

> On your Everything Watch, you receive a WhiskerWare brand holocat from someone using the name Satoshi Nakamoto...

你的智能表弹出一只 hologram 猫 —— 发件人：Satoshi Nakamoto。

> —“Bitcoin is not dying, but it needs your help. Don't forget the cat.”

“比特币不会死。但现在需要你的帮助。别忘了猫。”

> Holocat: “You better get to work. I can help, but you have to start meow.”

“快去干活。我帮你。现在就 meow。”

---

### Your first challenge

> Bitcoin is censorship-resistant money. Anybody can send money by broadcasting a transaction to the network...

比特币是抗审查货币。任何人都能广播交易，网络打包区块形成链。

> Satoshi Nakamoto... left a secret message in the very first bitcoin transaction.

中本聪在创世区块的第一笔交易里藏了一个秘密信息。  
你的首个任务：找出来，解码。

---

### Find the hidden message

> Find block height = 0 (the genesis block).

打开区块浏览器 → 找 height=0 的 Genesis Block

> Look at input called “Coinbase” → find SCRIPTSIG (HEX) → copy the hex payload

找到 `Coinbase` 输入 → 打开 `scriptsig` → 把 hex 字符串复制出来。

---

### Let's decode the message

> The message you found was encoded in HEX → convert to ASCII

把 hex 转 ASCII → 得到明文

> The decoded message references the front page of The Times on Jan 3, 2009

那句著名的报纸头条  
**这就是为何我们知道比特币创世纪 “不是偶然时间”**  
这就是其动机线索之一。

---

### What's in a transaction?

> Inputs & Outputs.

交易由输入 & 输出组成。  
上个挑战 decode 了 input 的隐藏 message  
这次 decode output —— `OP_RETURN`.

> Bitcoin has OP_RETURN so you can embed messages into TX outputs

BTC 用 `OP_RETURN` 也可以藏信息。

---

**( END of Chapter 1 narrative section )**