# Authenticated REST API

> Example using cUrl for authenticated API request assuming your API token is `abcdef1234567890abcdef1234567890`:

```bash
curl --user 'abcdef1234567890abcdef1234567890:' 'https://yourdomain.visitthem.org/api/v1/memberships/for_area/NY-1.json'
```

> Note the colon character at the end of the user credentials argument for specifying a blank password.

The Authenticated REST API allows customers to build applications that consume data exposed by VisitThem.org and it is designed to be used server-side.

We use Basic Authentication for authenticating HTTP requests, where the **username** component must be the API Token provided on Settings->General page on the admin back end and the **password** element is blank.

![API Token](/images/api_token.png)
