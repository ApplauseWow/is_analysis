# “修改用户信息”用例 [返回](../README.md)
## 1. 用例规约

|用例名称|修改用户信息|
|-------|:-------------|
|功能|修改用户个人信息|
|参与者|学生，老师|
|前置条件|必须先登录，并且查看用户的个人信息|
|后置条件| |
|主事件流| 1.用户填写用户信息 <br/> 2.用户提交修改信息 <br/>3.系统存储修改后的用户信息|
|备选事件流|1a. 如果用户输入的信息为空 <br/>&nbsp;&nbsp; 1.系统清空用户的该条信息|

## 2. 业务流程
无

## 3. 界面设计
- 界面参照: https://ApplauseWow.github.io/is_analysis_pages/final/selfinfo.html
- API接口调用
    - 接口1：[getSelfInfo](../interface/getSelfInfo.md)
    - 接口2：[saveSelfInfo](../interface/saveSelfInfo.md)
    
## 4. 算法描述
无
    
## 5. 参照表
- [User](../DataTables.md/#USERS)
- [Student](../DataTables.md/#STUDENTS)
- [Teacher](../DataTables.md/#TEACHERS)
