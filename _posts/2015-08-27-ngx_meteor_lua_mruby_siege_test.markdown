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
ngx_mruby
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

meteor
ransactions:            7894 hits
Availability:          78.94 %
Elapsed time:          21.31 secs
Data transferred:        46.97 MB
Response time:            1.85 secs
Transaction rate:       370.44 trans/sec
Throughput:           2.20 MB/sec
Concurrency:          686.42
Successful transactions:        7894
Failed transactions:          2106
Longest transaction:         10.16
Shortest transaction:         0.00

lua_ngx
ransactions:            1000 hits
Availability:         100.00 %
Elapsed time:           2.03 secs
Data transferred:         0.02 MB
Response time:            0.02 secs
Transaction rate:       492.61 trans/sec
Throughput:           0.01 MB/sec
Concurrency:            8.89
Successful transactions:        1000
Failed transactions:             0
Longest transaction:          1.01
Shortest transaction:         0.00
{% endhighlight %}
