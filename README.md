# jwt-test
JWT(JSON Web Token): 代替傳統 Session 辨識使用者的方式

## JWT 認證流程
* 前端傳送使用者資料 => 後端確認並找到該使用者資料 => 利用使用者資料與私鑰(自訂)創建 token
* => 將 token 傳給前端 => 前端將 token 存進 cookie => 每次要取得資源時會用此 token 放入 header 來取得資料

```js
// 前端的 request 都要帶上 token
{
  headers: {
    Authorization: `Bearer ${token}`
  }
}
```

## 參考
* JWT 簡單介紹: https://mgleon08.github.io/blog/2018/07/16/jwt/
* 有程式碼範例: https://andyyou.github.io/2016/06/09/implement-jwt-with-understanding/
