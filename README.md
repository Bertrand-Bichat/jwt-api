# Create new user

curl -XPOST -H "Content-Type: application/json" -d '{ "user": { "username": "YOUR_USERNAME", "password": "YOUR_PASSWORD", "age": YOUR_AGE } }' http://localhost:3000/users

# Login existing user

curl -XPOST -H "Content-Type: application/json" -d '{ "user": { "username": "YOUR_USERNAME", "password": "YOUR_PASSWORD" } }' http://localhost:3000/login

# Test if you are login with the 'auto_login'

curl -XGET -H "Content-Type: application/json" -H "Authorization: bearer YOUR_TOKEN" http://localhost:3000/auto_login
