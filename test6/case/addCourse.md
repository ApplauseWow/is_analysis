# “添加课程”用例 [返回](../README.md)
## 1. 用例规约

|用例名称|添加课程|
|-------|:-------------|
|功能|老师开设课程|
|参与者|老师|
|前置条件|添加课程之前，老师需要先登录|
|后置条件| 课程信息提交之后，系统自动保存课程信息，继续添加课程实验评分项|
|主事件流| 1.输入课程信息并提交 2.跳转添加实验评分项界面|
|备选事件流|1a. 课程信息每项不能为空 <br/>&nbsp;&nbsp; 1.提示用户重新输入|


## 2. 业务流程（顺序图）
无
    
## 3. 界面设计
- 界面参照: https://ApplauseWow.github.io/is_analysis_pages/final/addcourse.html

- API接口调用

    - 接口1：[getSelfInfo](../interface/getSelfInfo.md)
        
        获取教师个人信息以提交课程信息
        
    - 接口2：[addCourse](../interface/addCourse.md)
        
        保存课程信息
         
    
## 4. 算法描述
    无
    
## 5. 参照表

- [User](../DataTables.md/#USERS)
- [Teacher](../DataTables.md/#TEACHERS)
- [Course](../DataTables.md/#COURSES)