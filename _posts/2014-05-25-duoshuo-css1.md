---
author: stannis
date: 2014-5-25 10:20+08:00
layout: post
title: duoshuoCSS修改
slug: duoshuo
categories:
- 网页研究
tags:
- duoshuo
- CSS
---

**修改CSS如下**

{% highlight css %}
/*duoshuo style */
#ds-thread #ds-reset .ds-powered-by {
display: none !important;
}
#ds-thread #ds-reset .ds-meta {
display: none !important;
}
#ds-thread #ds-reset .ds-comments {
margin: 0 0 !important;
}
#ds-thread #ds-reset .ds-replybox {
margin: 0 0 !important;
}
#ds-thread #ds-reset .ds-post-toolbar span {
display:none !important;
}
{% endhighlight %}
<!--more-->
{% highlight css %}
#ds-thread #ds-reset #ds-bubble {
display:none !important;
}
#ds-thread #ds-reset .ds-avatar {
  background:none !important;
}
#ds-thread #ds-reset .ds-avatar img {
 -webkit-border-radius: 25px !important;
  -moz-border-radius: 25px !important;
  border-radius: 25px !important;
  -webkit-transition: -webkit-transform 0.4s ease-out;
  -moz-transition: -moz-transform 0.4s ease-out;
  transition: transform 0.4s ease-out;
}
#ds-thread #ds-reset .ds-avatar img:hover {
  -webkit-transform: rotateZ(360deg);
  -moz-transform: rotateZ(360deg);
  transform: rotateZ(360deg);
}
#ds-thread #ds-reset .ds-comment-body p {
color:#bbb !important;
}
#ds-thread #ds-reset .ds-login-buttons p {
color:#bbb !important;
}
{% endhighlight %}
