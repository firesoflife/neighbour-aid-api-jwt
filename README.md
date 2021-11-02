# JWT Auth for NeighbourAidApp

## Resources

- https://medium.com/binar-academy/rails-api-jwt-authentication-a04503ea3248

## Dependencies / Gems

- Rack Cors
- Bcrypt
- JWT

## Methodology

## Steps

1. Install gems -- add JWT, and uncomment rack-cors and bcrypt
2. Generate a "user" model ensuring you create columns for 'username', 'email', and 'password_digest'
3. Update the routes file

- Add resources for user with a param of `_username`
- Add the auth login route
- at a get request for application not found

4. Add teh JWT Secret Key file `lib/json_web_token.rb` to the `lib` directory

- Makes sending the encode and decode objects simpler and includes a token expiration time

5. Create the `authorize_request` function - responsible for authorizing user requests and ensuring token is sent in header
6. Build out user validation in `app/models/user.rb`
7. Add Crud functionality to UserController
8. Build out the Authentication Controller and add the Login feature
