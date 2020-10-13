# 星威矿池APP2.0 
	
### 获取用户昵称

#### Request
- Method: **POST**
- URL:  ```/userInfo```
- Headers：
- Body: {} 

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

### 修改用户昵称（新增）

#### Request
- Method: **POST**
- URL:  ```/updateNickName```
- Headers：
- Body:

```
{
     "id": String, // 用户id
     "nickName": String, //用户昵称
     
}
```

#### Response
- Body
{
  "code": 1,
  "msg": "success"
  "data": {}
}


### 获取用户节点矿池信息

#### Request
- Method: **POST**
- URL:  ```app/userProfit```
- Headers：
- Body: {}

#### Response
- Body
{
  "code": 1,
  "msg": "success"
  "data": 
  ```
  {
  	"totalNode": Number, // 我的节点数
	"lastDayProfit": String, // 昨日收益
  	"myPower": String, // 我的有效算力（新增）
	"storage": 
	{
		"effectiveStorage": Float, // 已使用
		"totalStorage": String // 总空间
	}
	
  }
      
  ```
}


### 获取矿池信息

#### Request
- Method: **POST**
- URL:  ```/app/miningPoolOverview```
- Headers：
- Body: {}

#### Response
- Body
{
  "code": 1,
  "msg": "success"
  "data": 
  ```
  {
      "poolNodes": [
	      { 
		"id": String, // 集群id
		"poolName": String, // 集群名称
		"storageSize": Number // 已用空间
		
	      }
      ], // 各集群存储空间使用情况
      "minerPower": Array, // 各集群有效算力
      "serverDayPower": Array, 
      "sevenDayProfit": Array, 
      "timelyInfo": 
	      {
		  "totalPower": 
			  {
			      "minerAdjPower": Float, // 星威矿池总算力
			      "totalAdjPower": Float, // 全网有效算力
			      "highLevel": Number, // 全网区块高度（新增）
			      "lockFile": String, // 全网总质押（新增）
			  },
		  "blockCount": Number, // 矿池创建区块量
		  "lockFile": String, // 矿池总质押
		  "currentlockFile": String, // 当前扇区质押 （新增）
		  "blockNewReward": String, // 最新区块奖励（新）
		  "blockAvgReward": String, // 24H平均收益（新）
	      }
      
  }
  ```
}
