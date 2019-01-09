---
layout: post
title:  "React deployment"
date:   2019-01-08 21:46:08 -0500
categories: jekyll update
author: "Luke"
---

哈喽大家好! 今天尝试了react project deployment

Deployment:

React:

https://facebook.github.io/create-react-app/docs/deployment#step-1-add-homepage-to-packagejson

先说废话:
Follow 了amazon S3的deployment 方法 (前后spend like an hour?...)
https://medium.com/@omgwtfmarc/deploying-create-react-app-to-s3-or-cloudfront-48dae4ce0af

结果貌似S3上只能是http的,然后aoundweb project里面有getLocation这种call, http通不过, 需要用https的网站才行,所以看了一下这个链接

https://medium.com/@itsmattburgess/hosting-a-https-website-using-aws-s3-and-cloudfront-ee6521df03b9

按要求去amazon route 53 register domain,结果居然需要等待通过(up to 3 days, 然后还有通不过的可能?)

于是我在等待中,deploy计划就先pending了

再说有用的:
Follow 了 Firebase 的 deploy

https://facebook.github.io/create-react-app/docs/deployment#step-1-add-homepage-to-packagejson

基本没遇到啥问题
就是一开始firebase init的时候,刚刚新创建的project没有show up,于是参照这个stackoverflow
https://stackoverflow.com/questions/50381048/new-project-not-showing-up-firebase-cli
就解决了

现在网站deploy在 https://aroundweb-9f2c4.firebaseapp.com/home
一切正常
