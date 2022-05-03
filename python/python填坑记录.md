## python填坑记录
### 版本差异
- 如下代码,`3.6.8`版本报错`SyntaxError: 'continue' not supported inside 'finally' clause`,`3.8.9`运行正常
  + [为什么在Python的`finally`子句中不允许`continue`？](https://www.thinbug.com/q/8302293)
  + [What’s New In Python 3.8 - Other Language Changes - 第一条](https://docs.python.org/3/whatsnew/3.8.html#other-language-changes)
  ```
  for i in range(10):
    print(i)
    try:
        pass
    except Exception as e:
        print(e)
    finally:
        continue
  ```