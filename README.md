# CDN
jsDelivr CDN

# 使用方法
```curl https://raw.githubusercontent.com/sure15/CDN/master/speedtest.sh | bash ```  

```curl https://raw.githubusercontent.com/sure15/CDN/master/superbench2.sh | bash ``` 单线程

```curl https://raw.githubusercontent.com/sure15/CDN/master/superbench3.sh | bash ``` 多线程
 
```curl https://raw.githubusercontent.com/sure15/CDN/master/superbench4.sh | bash ``` 单线程 精简版
 
```curl https://raw.githubusercontent.com/sure15/CDN/master/superbench5.sh | bash ``` 多线程 精简版

# 测速注意事项
1. 关闭bbr开启cubic。因为bbr流量机制，会导致小文件的测速不准确，但是我们浏览网页大部分不是视频而是小文件，如果是看视频，可以测试bbr开启的速度。(还是应该开启bbr，对于大文件来说，bbr流量控制是无敌的，小文件的话也轮不到bbr起作用)
2. 单线程测试的大概是100k文件的下载速度，多线程测试的大概是10m文件的下载速度。（不一定准确，仅猜测，简单说，多线程的测试已经是加入了流量控制）
3. 最好的测速网站[https://speed.cloudflare.com/](https://speed.cloudflare.com/)
