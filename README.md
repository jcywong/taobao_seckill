# taobao_seckill
淘宝、天猫半价抢购，抢电视、抢茅台，干死黄牛党
## 依赖
#### 安装chrome浏览器，根据浏览器的版本找到对应的[chromedriver](http://npm.taobao.org/mirrors/chromedriver/)下载安装

## web版使用说明
1、抢购前需要校准本地时间，然后把需要抢购的商品加入购物车  
2、如果要打包成可执行文件，可使用pyinstaller自行打包  
3、不需要打包的，直接在项目根目录下 执行 python3 main.py  
3.1、(可选)需要推送消息提醒（如微信/群机器人/短信)，在 https://sre24.com 免费注册得到推送 token，执行 `TOKEN=xxx python3 main.py`
4、程序运行后，会打开淘宝登陆页，需要自己手动点击切换到扫码登陆

#### 淘宝有针对selenium的检测，如果遇到验证码说明被反爬了，遇到这种情况应该换一个方案，凡是用到selenium都会严重依赖网速、电脑配置。
#### 如果想直接绕过淘宝的检测，可以手动打开浏览器登陆淘宝，然后再用selenium接管浏览器。只提供思路，具体实现大佬们可以自己摸索。




# jcy
1. 复制playwright_browsers目录到项目根目录下 
    - windows: C:\Users\YourName\AppData\Local\ms-playwright 
    - mac: /Users/YourName/Library/Caches/ms-playwright

2. 打包
```bash
 pyinstaller --onefile --add-data "playwright_browsers:playwright_browsers" --collect-all playwright main.py --noconsole
```

