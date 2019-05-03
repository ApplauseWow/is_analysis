# 接口：getStudentScores  [返回](../README.md)
用例： [查看课程成绩](../case/showScores.md)，[成绩评定](../case/giveScore.md)

- 功能：
    返回一个学生的所有实验成绩和实验评价以及该实验的评分细则。
    
- 权限：
    学生：只能查看自己的该课程成绩，即接口参数student_id必须等于登录学生的student_id，course_id等于点击进入的course_id
    老师：可以查看该学生的成绩以及对成绩评定。
    
- API请求地址： 
    接口基本地址/v1/api/getStudentScores/<student_id>&<course_id>

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学生的学号|
  |course_id|课程号|
    
- 返回实例：

        {         
            "status": true,
            "info": null,    
            "student_id": "201610414206", 
            "github_username": "ApplauseWow", 
            "class": "软件(本)16-2", 
            "name": "HolyKwok", 
            "total": 6,
            "avgresult":90.5,       
            "data": [
                {
                "test_id":1001, 
                "test_n":1
                "score": 91, 
                "review":"本实验做得好",
                "item":{
                    "实验完整":30,
                    "用例完整":30,
                    "有改进":40
                },
                "each_score":{
                    "1":30,
                    "2":30,
                    "3":31
                }
                }, 
                {
                ...其他实验
                }
            ] 
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |student_id|学号|
  |github_username|学生的gitHub用户名|
  |class|班级|
  |name|真实姓名|   
  |total|实验总数|  
  |data|所有实验的成绩和评语|
  |test_id|实验ID|
  |test_n|实验编号|
  |score|本实验成绩，可以为空，为空表示没有批改，没有批改的实验不入平均成绩，为0分则要计入平均成绩，所以成绩为空和为0是不一样的。|
  |review|本实验老师的评价，可以为空|
  |item|本实验各个评分细则|
  |each_score|各个评分细则得分|  

