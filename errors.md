## Frontend
```
[HPM] Error occurred while proxying request localhost:3000/story/getAllStories?search=&page=1 to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)
[HPM] Error occurred while proxying request localhost:3000/auth/private to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)  
```

[Node.js v18.3.0 documentation - Common system errors](https://nodejs.org/api/errors.html#errors_common_system_errors)
> `ENOTFOUND` (DNS lookup failed): Indicates a DNS failure of either `EAI_NODATA` or `EAI_NONAME`. This is not a standard POSIX error.
