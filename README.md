## 1.新建ibm账号
>ibm云服务  https://cloud.ibm.com/
创建Cloud Foundry 应用程序---go应用
然后进入右上角的cmd

wget --no-check-certificate -O ibmcloud.sh https://raw.githubusercontent.com/Qa7060123/ibm/master/ibmv2ws.sh && chmod +x ibmcloud.sh  && ./ibmcloud.sh

## 2.CDN
>加速https://www.cloudflare.com/
新建一个workers
```
addEventListener(
  "fetch",event => {
     let url=new URL(event.request.url);
     url.hostname="v2rayy1234.us-south.cf.appdomain.cloud";
     //域名在v2ray配置里
     let request=new Request(url,event.request);
     event. respondWith(
       fetch(request)
     )
  }
)
```
>地址写测试cf后最好的ip，伪装域名写你的cf域名

![v2ray](https://raw.githubusercontent.com/Qa7060123/ibm/master/ibm.jpg)
