# Building and running on localhost

```bash
git clone git@github.com:Bertrand-Bichat/jwt-api.git
cd jwt-api
bundle install
yarn install
rails db:create db:migrate db:seed
rails s
http://localhost:3000/
```

# Test repo

## Create new user

```bash
curl -XPOST -H "Content-Type: application/json" -d '{ "user": { "username": "YOUR_USERNAME", "password": "YOUR_PASSWORD", "age": YOUR_AGE } }' http://localhost:3000/users
```

## Login existing user

```bash
curl -XPOST -H "Content-Type: application/json" -d '{ "user": { "username": "YOUR_USERNAME", "password": "YOUR_PASSWORD" } }' http://localhost:3000/login
```

## Test if you are login with the 'auto_login'

```bash
curl -XGET -H "Content-Type: application/json" -H "Authorization: bearer YOUR_TOKEN" http://localhost:3000/auto_login
```
