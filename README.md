# 我们 + 你 = ∞

感谢你对 [RightCapital LLC](http://join.rightcapital.com/) 的后端开发工程师一职感兴趣。我们为你准备了几个技术上的问题。你可以查阅资料，但请务必独立完成。我们会在电话面试中听取你的答案并作出反馈。

### 问题一：

输出 10,000 以内的`三生素数`，以换行符分隔。

> 注意：
- 请使用 PHP 实现。
- 尽可能减少程序运行时间。
- 请将结果使用 [gist](https://gist.github.com/) 提前发送到 `yaodong.zhao@rightcapital.com`。


####PHP代码

~~~PHP
<?php
	//(P P+2 P+6)

	//判断是否为素数
	function IsPrime($n)
	{
		if($n < 2)
		{ 
			return false;
		}
		
		if($n == 2)
		{
			return true;
		}

		for($i = 2 ;$i <= sqrt($n) ;$i++)
		{
			if($n % $i == 0)
			{
				return false;
			}
		}
		return true;
	}

	$totlal = 0;
	for($n = 1;$n < 10000;$n++)
	{
		if(IsPrime($n) && IsPrime($n+2) && IsPrime($n+6))
		{
			$total++;
			$m = $n + 2;
			$p = $n + 6;
			echo "(".$n."	".$m."	 ".$p.")"."<br>";
			$n+=5;//改进算法
		}
	}
	echo "total: ".$total."<br>";

~~~




### 问题二：

我们已经有了一个爬虫程序（Spider）来为我们抓取某种股票数据。现在需要一个新的程序（Manager）负责这些数据的存储和检索。

那么，如果你来负责这个程序的开发：

- 你需要了解哪些技术细节？
- 为什么需要了解这些技术细节？

> 注意：
- 你只需要在电话中口述。
- 你可以事先做好笔记。
- 假设只单独使用一台服务器，配置 32 G RAM 和 8 CPU Cores，充足的硬盘存储空间。
- 你可以使用 PHP 5.5，MySQL 5.5，Redis 2.8.19。
- 你可以根据自己的经验，尽可能多地提问。

### 问题三：

使用尽可能简单的语言讲解 OAuth 协议。

> 注意：
- 你只需要在电话中口述。
- 你可以事先做好笔记。
