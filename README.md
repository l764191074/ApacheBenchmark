# 这是一个ApacheBenchmark代替程序 目前实现的功能有
主要使用的模块
optparse
multiprocessing.pool
requests
re
实现的命令行参数
    -n requests     Number of requests to perform
    -c concurrency  Number of multiple requests to make
    -t timelimit    Seconds to max. wait for responses
    -p postfile     File containing data to POST
    -T content-type Content-type header for POSTing
    -C attribute    Add cookie, eg. 'Apache=1234. (repeatable)
    -H attribute    Add Arbitrary header line, eg. 'Accept-Encoding: gzip'
                    Inserted after all normal header lines. (repeatable)
    -X proxy:port   Proxyserver and port number to use
    -s F or T       如果连接是是http设置为F https为T  默认是F
    -S              Do not show confidence estimators and warnings.
    -h              Display usage information (this message)
举例：
python apache_benchmark.py -u www.baidu.com -c 4 -n 20 -T text/html;charset=utf-8 -C SIGNIN_UC=70a2711cf;sdsda=sdasd1;sdasda=sdasdasdad2 -s T -S T -t 300
