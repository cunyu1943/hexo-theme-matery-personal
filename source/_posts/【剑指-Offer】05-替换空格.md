---
title: 【剑指 Offer】05. 替换空格
mathjax: true
toc: true
tags:
  - 剑指 Offer
categories:
  - Online Judge
abbrlink: 3a6d4dac
date: 2021-05-04 16:36:14
top:
---

>   **本文已收录至个人 Github仓库**：[cs-docs](https://github.com/cunyu1943/cs-docs)，欢迎各位 **Star、Fork** ~

## 题目

- [剑指 Offer 05. 替换空格](https://leetcode-cn.com/problems/ti-huan-kong-ge-lcof/)
- 难度：简单

## 描述

>   请实现一个函数，把字符串 `s` 中的每个空格替换成"%20"。
>
>   **示例 1：**
>
>   **输入**：s = "We are happy."
>
>   **输出**："We%20are%20happy."
>
>   **限制：**
>
>   0 <= s 的长度 <= 10000

## 方法

### 思路

1.  遍历字符串，对字符串中的每个字符进行判断；
2.  若字符等于空格，则将字符串 `result` 加上 `%20`；
3.  若不等于空格，则将字符串 `result` 加上字符串当前字符；
4.  主要进行数组的遍历操作，所以时间复杂度为 $O(n)$；

### 实现

```java
public String replaceSpace(String s) {
    StringBuilder resutl = new StringBuilder();
    for (int i = 0; i < s.length(); i++) {
        if (s.charAt(i) != ' ') {
            resutl.append(s.charAt(i));
        } else {
            resutl.append("%20");
        }
    }
    return resutl.toString();
}
```

>   建议关注公众号 「**村雨遥**」，最新干货文章不容错过 ~

