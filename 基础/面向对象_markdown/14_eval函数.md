# `eval` 函数

`eval()` 函数十分强大 —— **将字符串** 当成 **有效的表达式** 来求值 并 **返回计算结果**

    # 基本的数学计算
    In [1]: eval(&quot;1 + 1&quot;)
    Out[1]: 2

    # 字符串重复
    In [2]: eval(&quot;&#39;*&#39; * 10&quot;)
    Out[2]: &#39;**********&#39;

    # 将字符串转换成列表
    In [3]: type(eval(&quot;[1, 2, 3, 4, 5]&quot;))
    Out[3]: list

    # 将字符串转换成字典
    In [4]: type(eval(&quot;{&#39;name&#39;: &#39;xiaoming&#39;, &#39;age&#39;: 18}&quot;))
    Out[4]: dict
    `</pre>

    ## 案例 - 计算器

    **需求**

1.  提示用户输入一个 **加减乘除混合运算**
2.  返回计算结果

    <pre>`input_str = input(&quot;请输入一个算术题：&quot;)

    print(eval(input_str))

    `</pre>

    ## 不要滥用 `eval`

    > 在开发时千万不要使用 `eval` 直接转换 `input` 的结果

    <pre>`__import__(&#39;os&#39;).system(&#39;ls&#39;)
    `</pre>

*   等价代码

    <pre>`import os

    os.system(&quot;终端命令&quot;)

*   执行成功，返回 0
*   执行失败，返回错误信息