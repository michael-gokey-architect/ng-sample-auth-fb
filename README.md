# ng-sample-auth-fb
a sample angular app doing auth with facebook


JSON Web Tokens are an open, industry standard RFC 7519 method for representing claims securely between two parties

A token Encoded looks like this:
- eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c

When Decoded, it shows the 3 parts:
HEADER:ALGORITHM & TOKEN TYPE
```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

PAYLOAD:DATA
```json
{
  "sub": "1234567890",
  "name": "John Doe",
  "iat": 1516239022
}
```

VERIFY SIGNATURE
```json
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
your-256-bit-secret
) secret base64 encoded
```