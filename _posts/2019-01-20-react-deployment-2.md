---
layout: post
title:  "React Deployment 2 - npm run build blank page, http within https website"
date:   2019-01-20
categories: jekyll update
author: "Luke"
---

### Always develop website in the incognito (private) mode!

1. An error in the component might cause it to be not rendered on the
html. E.g., if the error is in your Main.js, and all your other components is
within your Main.js, your website could ended up rendering as a blank page.
(Ever wondering where are all the components?)

2. During development, frequently follow the following steps to avoid surprise
during deployment:
    1. develop and ```npm start``` and check the website on localhost
    
    2. ```npm run build``` to build the project
    
    3. ```serve -s build``` to serve the build created in the previous step
    
    4. even try to deploy it on firebase and see if it works as at local

3. If the browser is complaining about you are sending http requests
within the https website. You could add the following line inside the index.html's
head tag: 
```
<meta http-equiv="Content-Security-Policy" content="upgrade-insecure-requests">
``` 
. It will upgrade all http requests to https requests. Of course, the https
requests need to be backed up by the website you are sending requests to in
order for this to be work.

Thanks to https://stackoverflow.com/questions/33507566/mixed-content-blocked-when-running-an-http-ajax-operation-in-an-https-page


