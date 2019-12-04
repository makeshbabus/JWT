# JWT

POSTMAN

localhost:5000/user/login
POST
Body Raw
{
"username":"user123",
"password": "1234"
}
Headers
Content-Type application/json


GET
localhost:5000/user/data
Headers
Content-Type application/json
Authorization Bearer pasteCopiedTokenLikeeyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9

//authToken variable should have token assigned from result of login api localhost:5000/user/login
fetch('/user/data', {
  method: 'GET',
  headers: {
    'Authorization': 'Bearer' + authToken
  }
})
.then(res => res.json())
.then(data => { console.log(data) })
.catch(err => { console.log(err) })

Reference:
https://medium.com/@maison.moa/using-jwt-json-web-tokens-to-authorize-users-and-protect-api-routes-3e04a1453c3e

npm install --save jsonwebtoken
