# 星威矿池APP2.0 
	
### 获取用户昵称

#### Request
- Method: **POST**
- URL:  ```/userInfo```
- Headers：
- Body:

```
{}
```

#### Response
- Body
{
  "code": 1,
  "msg": "success"
  "data": 
  
  ```
  {
  
      "id": String, // 用户id
      "phoneNum": String, // 手机号
      "nickName": String, //用户昵称
      "fullName": String, // 用户姓名
      "email": String,// 绑定邮箱
      "idCardStatus" : Number, // 实名状态
      "verifyIdCardMsg" : String, // 审核备注信息
      "googleAuthStatus" : Number, // 谷歌认证状态
  }
  ```
}

