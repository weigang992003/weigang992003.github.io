---
layout: post
title:  "js cross domain"
date:   2016-09-30 16:11:00
categories: literature
---
js in client brower

```javascrpt
var url = "http://server.com";
var getAuthData = function (user, password) {
var formdata = new FormData();
  formdata.append('user', user);
  formdata.append('password', password);
  return formdata;
};
var peaboxLogin = function (user,password) {
  var _login = function () {
    var authData = getAuthData(user, password);
    $.ajax({
      url: url,
      type: "POST",
      contentType: false,
      processData: false,
      crossDomain: true,
      data: authData,
      xhrFields: {
       withCredentials: true
      },
      success: function (response) {
        console.log(response);
      },
      error: function (err, status, code) {
        if (err.status == 0) {

        } else {

        }
      }
    });
  };
  _login();
};


```

Server side should allow origin

```php
header("Access-Control-Allow-Origin: http://client.com");

header("Access-Control-Allow-Credentials: true");
```
