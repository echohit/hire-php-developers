# 我们 + 你 = ∞

感谢你对 [RightCapital LLC](http://join.rightcapital.com/) 的后端开发工程师一职感兴趣。我们为你准备了几个技术上的问题。你可以查阅资料，但请务必独立完成。我们会在电话面试中听取你的答案并作出反馈。

### 问题一：

输出 10,000 以内的`三生素数`，以换行符分隔。

> 注意：
- 请使用 PHP 实现。
- 尽可能减少程序运行时间。
- 请将结果使用 [gist](https://gist.github.com/) 提前发送到 


####PHP代码


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


- 前端： [frontend.md]
- 后端： [backend.md]


# 后端招聘题目

## Part I

用简洁准确的语言回答以下问题。

- OAuth 协议是如何保证安全的？
- ORM 有哪些优点和缺点?

可选题目：

有如下两种典型的设计模式，简述你对两者的评价：

- Yii Framework Components
- Laravel Facade

## Part II

使用 PHP + MySQL 编写一个软件，实现以下目标：

- 从 Yahoo Finance 抓取 Apple Inc. 指定日期范围内的每日收盘价。
- 将数据存储存储到 MySQL。

可选题目：

- 使用 HighCharts 显示股价走势图。
- 求出查询日期内的收盘价的平均值。

## Part III

在工作中，你看到了这么一段代码：

```php
class Category
{
    public function filter($check, $check2 = null)
    {
        $new_arr = [];
        while ($i < count($this->list)) {
            if (strpos($this->list[$i], $check) || strpos($this->list[$i], $check2))
              $new_arr[] = $this->list[$i];
            $i++;
        }
        return $new_arr;
    }
}
```

经过了解，这段代码是用来将分类数组中特定的几项筛选出来，然后在页面上显示。但是这个解决方案和代码都是很糟糕的。于是你需要：

- 列出这个解决方案和这段代码所存在的问题。
- 重构。

