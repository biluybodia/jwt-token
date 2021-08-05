# JWT authentication plugin

For generation a JWT-token used jwt authentication plugin (https://wordpress.org/plugins/jwt-authentication-for-wp-rest-api/)

# Setting plugin and usage 

- After activation plugin from your admin panel you available next endpoint "/wp-json/jwt-auth/v1/token". Create a new request to this endpoint using your credentional from wp-admin and get in the response JWT-token and additional parameters (can be change).
- Use this JWT-token for login in the website without login and password. For it you need a pass this JWT-token to HEADER as Bearer token.

# Example

As result in the a file "functions.php" you can find a filter "rest_authentication_errors". Combination this filter and plugin can help decide available API Wordpress only for authorization users.
Also in the a file "functions.php" your can find a filter "jwt_auth_token_before_dispatch" where was added additional parameters for JWT-token.