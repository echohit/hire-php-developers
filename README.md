# 我们 + 你 = ∞

## 关于我们

> 我们是一个位于美国／香港／北京的创业公司，我们致力于创建一个面向美国市场的专业金融服务网站。
> 关于招聘要求，薪资福利，项目发展请参考 https://careers.ngfplanner.com/ 。

我们目前在工作中使用的部分软件、工具或服务：

- Atlassian: JIRA, Confluence, HipChat, Stash, Bamboo, SourceTree
- Google Apps, AWS, GAE, Logentries, NewRelic, MailGun, Stripe, Apiary, Pixelapse
- PHPStorm, Sublime, VIM

我们要求代码和解决方案的优雅简洁，即使是在生产环境。

我们只招聘有共同世界观和价值观的人，不会有不容易相处的同事。

## 如何做题

- 时间：自选一周时间独立完成，可以查询或者参考任何资料，最好不依赖其他框架和库。
- 提交：请将代码提交到 Github 或者 BitBucket，然后将 URL 发送到 austin@ngfplanner.com

## 开始做题

- 前端： [frontend.md](frontend.md)
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

