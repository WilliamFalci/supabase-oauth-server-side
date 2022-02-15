# supabase-oauth-server-side
Use the Auth token in your server-side (Nodejs Tested)

## Explanation

This middleware is created to be integrated with NodeJS + Express + Supabase

## Usage:

### Server:
1. Copy the file where you want inside your project
2. Import the file into the route you need to validate ```const supabase_middleware = require('../config/supabase_middleware')```
3. Invoke the middleware parsing `req` and `res`: ```const {user,supabase} = await supabase_middleware(req,res);```
4. If the validation would be OK then you will get ```user``` and ```supabase```, the user will contain the user details, supabase will be the istance with the current session to use for your next logical calls
5. If the validation would be KO then the middleware will automatically sent the error

---

### Client Call:
1. Login using the [supabae.auth-signin](https://supabase.com/docs/reference/javascript/auth-signin)
2. Parse the `access_token` under ```currentSession``` into Authentication: Bearer to your endpoint

#### Enjoy
