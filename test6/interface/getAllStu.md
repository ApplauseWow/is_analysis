# 接口：getAllStu  [返回](../README.md)
用例： [查看学生列表](../case/showStuList.md)

- 权限：
    老师：可以看到所授课学生信息和成绩。

- 功能：
    返回所有授课学生的列表。

- API请求地址：
   接口基本地址/v1/api/getAllStu/<course_id>

- 请求方式 ：
    GET

- 请求参数说明:
    |参数名称|说明|
    |:---------:|:--------------------------------------------------------|      
    |course_id|课程的ID号。|

- 返回实例：

        {
            "status": true,
            "info": null,
            "total": 121,
            "data": [
                {
                    “stu_info”:{
                        "github_username":"ApllauseWow"
                        "stu_id":"201610414206",
                        "name":"HolyKowk",
                        "claz":"2",
                        ...    
                    },
                    "stu_score":{
                        "test_1":"90",
                        "test_2":"85",
                        "test_3":"88",
                        ...
                    }
                },
                {
                ...其他学生
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回学生人数|
  |data|所有学生的信息成绩映射关系数组|
  |stu_info|学生基本信息列表|
  |GITHUB_USERNAME|GITHUB 用户名|
  |STUDENT_ID|学号|
  |CLAZ|班级|
  |NAME|真实姓名|
  |stu_score|学生成绩列表|
  |test_1|第一次试验成绩|
  |test_2|第二次实验成绩|
  |test_3|第三次实验成绩|