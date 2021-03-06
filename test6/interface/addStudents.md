# 接口：addStudents  [返回](../README.md)
用例： [添加学生](../case/addStudents.md)

- 权限：
    老师：登录后并且已经添加了课程和课程评分细则后才能添加学生。

- 功能：
    添加授课学生。

- API请求地址：
   接口基本地址/v1/api/addStudents/

- 请求方式 ：
    POST
    
- 请求实例 ：

        {
            "course_id":"10000001",
            "stu":[
                {
                    "school":"成都大学",
                    "年级":"2016",
                    "班":2,
                    "专业":"软件工程"
                },
                {
                    ...其他班级
                }
            ]
        }

- 请求参数说明:

    |参数名称|说明|
    |:---------:|:--------------------------------------------------------|      
    |course_id|添加课程时生成的课程号|
    |stu|班级列表，根据学校、班级、专业从Student导入学生，生成对应的成绩表|

- 返回实例：

        {
            "status": true,
            "info": null,
       
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|

