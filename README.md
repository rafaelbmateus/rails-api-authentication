#Sample - Rails API
...

##Setup
```
bundle install
rake db:create
rake db:migrate
rake db:seed
rails s
```

##Consuming the API

####Signup - users#create
```bash
curl -X POST -H "Content-Type: application/json" -d '{"user": {"username": "testuser", "email": "tests@example.com", "password": "12341234", "password_confirmation": "12341234"}}' http://localhost:3000/v1/users

>> {"email":"email@example.com","username":"Your Name","token_type":"Bearer","user_id":2,"access_token":"2:cccyXLZ7o_XpK6MxU_Bt"}
```

####Login - sessions#create
```bash
curl -X POST -H "Content-Type: application/json" -d '{"email": "test@example.com", "password": "12341234"}' http://localhost:3000/v1/login

>> {"email":"test@example.com","username":"testuser","token_type":"Bearer","user_id":12,"access_token":"12:cccyXLZ7o_XpK6MxU_Bt"}
```

####Get Users - users#index
curl -X GET -H "Content-type: application/json" -H "Aution: 1:F8ANpLpQzhs2mEUviv8y" http://localhost:3000/v1/users
