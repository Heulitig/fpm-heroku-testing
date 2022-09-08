# fpm-heroku-testing

This is meant to initially test deployment of `rust binary` on heroku and once it's done will proceed towards deployment of `fpm binary` and serve package on heroku from its `download-base-url`.

## FPM Command to serve package from its download base url
```
fpm serve --download-base-url=<package-url>
```

Later Github action hook will be added to invalidate cache on erery Github push on the main branch. 
For that will create a .yml file will be call
`https://<package-url>/-/clear-cache/?package=main&all-dependencies=true.`
