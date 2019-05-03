
# 数据库设计 [首页](./README.md)
    
<div id="USERS"></div>

- ## User表（用户表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |USER_ID|NUMBER(8,0)|主键|否| | | 用户ID|
    |NAME|VARCHAR2(50 BYTE)| |否| | | 用户真实姓名|
    |GITHUB_USERNAME|VARCHAR2(50 BYTE)| |是|空| | GitHUB用户名|
    |PASSWORD|VARCHAR2(512 BYTE)| |是|空| | 加密存储密码，为空表示密码就是学号|
   
<div id="TEACHERS"></div>

- ## Teacher表（老师表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |TEACHER_ID|VARCHAR2(50 BYTE)|主键|否| | | 老师的编号|
    |USER_ID|NUMBER(8,0)|外键|是| | | 老师的用户ID，USERS表的外键|
    |DEPARTMENT|VARCHAR2(400 BYTE)| |否| | | 老师属于的部门|
    |SCHOOL|VARCHAR2(400 BYTE)| |否| | | 老师所在的学校|

<div id="STUDENTS"></div>

- ## Student表（学生表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |STUDENT_ID|VARCHAR2(50 BYTE)|主键|否| | | 学生的学号|
    |USER_ID|NUMBER(8,0)|外键|是| |空| 学生的用户ID，USERS表的外键，为空表示还没有建立用户| 
    |MAJOR|VARCHAR2(20 BYTE)| |否| | |学生的专业|   
    |CLAZ|VARCHAR2(20 BYTE)| |否| | |学生的班号|
    |GRADE|VARCHAR2(20 BYTE)| |否| | |学生的年级|
    |SCHOOL|VARCHAR2(400 BYTE)| |否| | |学生所属学校|

<div id="COURSES"></div>

- ## Course表（课程表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |COURSE_ID|VARCHAR2(50 BYTE)|主键|否| | | 课程号|
    |TEACHER_ID|VARCHAR2(50 BYTE)|外键|否| | |教师工号| 
    |NAME|VARCHAR2(20 BYTE)| |否| | |课程名称|
    |TERM|VARCHAR2(20 BYTE)| |否| | |开课学期|

<div id="GRADES"></div>

- ## Score表（学生实验成绩表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |TEST_ID|VARCHAR2(50 BYTE)|联合主键1，外键|否| | | 实验ID，Test表外键|
    |STUDENT_ID|VARCHAR2(50 BYTE)|联合主键2，外键|否| | | 学生的学号，Student表外键|
    |SCORE|NUMBER| |是|空| 取值0-100| 分数，这个值为空表示没有批改|
    |REVIEW|VARCHAR2(400 BYTE)| |是|空| | 老师对实验的评语|
    |EACH_SCORE|VARCHAR2(50 BYTE)| |是|空|  | 每个评分项分数组成的字符串，用分隔符分开|
    
<div id="TESTS"></div>

- ## Test表（实验项目表）

    |字段|类型|主键，外键|可以为空|默认值|约束|说明|
    |:-------:|:-------------:|:------:|:----:|:---:|:----:|:----------|
    |TEST_ID|VARCHAR2(50 BYTE)|主键|否| | | 实验ID|
    |COURSE_ID|VARCHAR2(50 BYTE)|外键|否| | | 课程ID|
    |TEST_NUM|NUMBER(6,0)| |否| | | 实验编号|
    |SCORE_ITEM|VARCHAR2(400 BYTE)| |是|空| | 实验的评分项，中间有分割符隔开各个评分项|
