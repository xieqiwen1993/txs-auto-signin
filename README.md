# txslicai.com-auto-signin

## system requirement:
- mac os, test on version 10.11.1 (15B42)


## dependency

- [phantomjs](http://phantomjs.org/), you need install the binary file to /usr/local/bin/phantomjs or link to this path,
if you do not want install to this path, you need to update the first line to specify your binary path in every .js file
- [nodejs](https://nodejs.org/en/)

**the phantomjs binary on official website does not work, you can download  phantomjs from [github](https://github.com/eugene1g/phantomjs/releases)**

- linux module libicu, you can install it by `sudo yum install libicu`
## usage

if you are already login:

`./signin.js week` to sign in one week  or `./signin.js day` to sign in today

if you are not login:

1. send code to your mobile, `./send_code.js {your_mobile_number}`
2. after receiving the code, `./signin.js {your_mobile_number} {code}`
3. after login, `./signin.js week` to sign in one week  or `./signin.js day` to sign in today


ps:when you are login, your login state will store in cookiejar.json and you do not need to login when next sign in,
pay attention to this file, **do not upload it to github or anyother website, keep it yourself**