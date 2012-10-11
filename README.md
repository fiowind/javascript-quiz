# JavaScript 测试

**说明:**

这个测试不是玩一些奇javascript淫技巧来让颇费思量，而是用来方便招聘人员筛选前端开发人员，其主要目的就是为了pass掉那些只会用jQuery而不懂javaScript底层的应聘者。


## Intro Questions

01. When might comparative type coercion occur? How would you avoid it? How would you change a "falsy" or "truthy" value into a real boolean?

02. 描述下变量作用域是怎么工作的，如何用匿名函数去创建一个能立即执行的闭包。

03. 简要介绍下原型继承和传统的类继承的区别

04. Describe how the "module pattern" works. Explain how the "revealing module pattern" expands upon it.

05. 浏览器端的MVC(或者MVVM)工作机制是什么？你用过哪些MVC(MVVM) JS框架？

## 附加问题

06. 以下计算结果为啥不同？

    ```js
    '1' + 2 +  3 ; // 等于 '123'
     3  + 2 + '1'; // 等于 '51'
     3  + 2 +  1 ; // 等于 6
    ```

07. 为什么 `0.3` *不是* 预期的计算结果，如何得到正确的计算结果呢？

    ```js
    0.1 + 0.2; // 结果为 0.30000000000000004
    ```

08.  描述下什么是变量声明提升(variable hoisting),如何避免变量生命提升可能导致的问题？

09. 如下的代码有什么区别？

    ```js
    function foo() {}

    // 另外一种写法

    var foo = function() {};
    ```

10. 什么时候用call函数，什么时候用apply函数，它们有啥区别？

11. 如何判断一个变量是对象还是数组. (*提示:* `typeof` 返回结果不一定准确!)

12. 在下面的代码中，foo代表什么? (*提示:* 需要弄清楚 `this` 代表什么.)

    ```js
    (function(foo) {
      // 'foo'指代什么？
    })(this);
    ```

13. 在Javascript(和DOM)中，一些诸如`window`、`document`、`undefined`的全局变量并不是一成不变的，用户可能会对它们重新赋值，如何保证我们用的这些内置变量是最原始的值而不是用户修改过的(*提示:* 参考上一个问题 )，如下面的代码所示：

    ```js
    var window = '';
    var document = 0;
    var undefined = true;
    ```

14. 请用一句代码来复制一个数组

15. What is the difference between `setInterval` and `setTimeout`? *Bonus:* What is the lowest cross-browser increment that each can accurately use? `setInterval`和 `setTimeout`有啥区别? 

16. 解释下`delete`是如何工作的，什么类型的变量不可删除?

17. 解释下事件委托是如何工作的，在UI交互时，什么情况下该用事件委托呢？如下面的例子所示&hellip;

    ```html
    <ul id="special">
      <li>
        <a href="#">Special link 1</a>
      </li>
      <li>
        <a href="#">Special link 2</a>
      </li>
      <li>
        <a href="#">Special link 3</a>
      </li>
    </ul>
    ```

18. 下面代码的作用是什么?

    ```js
    var foo = bar ? bar : 0;
    ```

19. 你在什么情况下会写下面的代码？这样的代码可能存在什么问题？

    ```js
    foo && foo.bar();
    ```

20. `parseInt` 和`parseFloat` 有啥区别? 什么时候需要调用数字的`toFixed()`方法? 下面的代码在什么情况下会有用处?

    ```js
    var my_number = my_string - 0;
    ```

21. 写一个名为 `sum` 的函数，它能返回所有参数的总和. 使用如下所示&hellip;

    ```js
    // 结果为15
    sum(1, 2, 3, 4, 5);

    // 结果为0
    sum(5, null, -5);

    // 结果为10
    sum('1.0', false, 1, true, 1, 'A', 1, 'B', 1, 'C', 1, 'D', 1, 'E', 1, 'F', 1, 'G', 1);

    // 结果为 0.3, 而不是 0.30000000000000004
    sum(0.1, 0.2);
    ```