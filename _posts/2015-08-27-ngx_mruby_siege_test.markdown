---
layout: post
title: 'ngx_mruby_siege_test'
date: 2015-08-27 14:29:00
categories: ruby
---
{% highlight sh %}
tool: siege
commands: siege -c 10000 -r 1 -f test.url
Mem:   3924680k total
cpu MHz   : 3392.294
processor : 1
ransactions:            5000 hits
Availability:         100.00 %
Elapsed time:           9.22 secs
Data transferred:         0.14 MB
Response time:            0.01 secs
Transaction rate:       542.30 trans/sec
Throughput:           0.02 MB/sec
Concurrency:            4.01
Successful transactions:        5000
Failed transactions:             0
Longest transaction:          0.13
Shortest transaction:         0.00

{% endhighlight %}
