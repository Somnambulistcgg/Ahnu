# Ahnu

安徽师范大学教务系统的部分爬虫， 以及使用样例。

## Base.py
使用教务系统的基础文件：
  1. `get_page()` 获取某一页面，注意学校教务系统的Set-Character，requests无法解析。必须用content手动解码为“UTF-8”。
  2. `cache` 保持登陆状态的值，可以使用`cache`的`get`和`post`方法进行其他操作。

## ChoseLessons.py
选课:

  课程编号可通过审查元素查看, 为任一tr的id.例如`id="2017-2018-1-07492110-0101224-1"`, 则课程编号为 `(2017-2018-1)-07492110-0101224-1`

## GetTranscript.py
查询成绩:

  登录后Get请求`http://jwgl.ahnu.edu.cn/query/cjquery/index?action=ok&xkxn=学年&xkxq=学期`

  学年应类似于`2017-2018`； 学期应为`1`或`2`，其他值会直接返回整个学年的所有成绩

## WriteTeachingEvaluation.py
  None
