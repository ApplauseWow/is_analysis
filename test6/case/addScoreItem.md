# “添加课程评分细则”用例 [返回](../README.md)
## 1. 用例规约

|用例名称|添加课程评分细则|
|-------|:-------------|
|功能|老师添加实验评分项|
|参与者|老师|
|前置条件|添加课程评分细则之前，老师需要先登录并且添加课程|
|后置条件| 评分项提交之后，系统自动保存评分项|
|主事件流| 1.输入课程评分细则信息并提交|
|备选事件流|1a. 课程评分细则信息每项不能为空 <br/>&nbsp;&nbsp; 1.提示用户重新输入|


## 2. 业务流程（顺序图）
无

## 3. 界面设计
- 界面参照: https://ApplauseWow.github.io/is_analysis_pages/final/addscoreitem.html

- API接口调用

    - 接口1：[addScoreItem](../interface/addScoreItem.md)
        
        保存提交实验评分项
         
    
## 4. 算法描述
    无
    
## 5. 参照表
- [Course](../DataTables.md/#COURSES)
- [Test](../DataTables.md/#TESTS)
