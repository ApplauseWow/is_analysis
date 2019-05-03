
# 接口：getSelfInfo  [返回](../README.md)
用例： [查看用户信息](../case/showSelfInfo.md),[修改用户信息](../case/modifySelfInfo.md)

- 功能：
    查看用户的所有信息。
    
- 权限：
    学生/老师：查看自己的信息，必须先登录。    
    
- API请求地址： 
    接口基本地址/v1/api/getSelfInfo/<user_id>

- 请求方式 ：
    GET
      
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  
- 返回实例：

        {         
            "status": true,
            "info": null,
            "ID":"201610414206",    
            "name":"HolyKowk",
            "claz":"2"
            "github_username":"ApplauseWow",
            "type":"学生" ,
            ...           
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |ID|学号或者工号|
  |name|用户的真实姓名|  
  |claz|所属班|
  |github_username|gitHub用户名|
  |type|用户类型：老师或者学生|