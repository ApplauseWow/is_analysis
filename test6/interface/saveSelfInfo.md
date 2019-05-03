# 接口：saveSelfInfo  [返回](../README.md)
用例： [修改用户信息](../case/modifySelfInfo.md)

- 功能：
    修改用户的个人信息。
    
- 权限：
    学生/老师：必须先登录。    
    
- API请求地址： 
    接口基本地址/v1/api/saveSelfInfo

- 请求方式 ：
    POST

- 请求实例：

        {
            "id":"201610414206",
            "github_username":"ApplauseWow", 
            "name":"HolyKwok",
            ...           
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  |github_username|用户GitHub用户名。| 
  |name|用户姓名|
  |...|...|
  
- 返回实例：

        {         
            "status": true,
            "info": null
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|