# Cloud189Checkin  
forked from peng4740/Cloud189Checkin-Actions  
天翼云盘每天签到1次，抽奖2次  

登录看的以下项目：
> [Cloud189](https://github.com/Dawnnnnnn/Cloud189)
> [cloud189](https://github.com/Aruelius/cloud189)

# Github Actions说明
## 一、Fork此仓库
![](http://tu.yaohuo.me/imgs/2020/06/f059fe73afb4ef5f.png)
## 二、设置账号密码
添加名为**USER**、**PWD**、**WWBOT**(可选)、**DDBOT**(可选)、**SCKEY**(可选)的变量  
值分别为**账号**、**密码**、**企业微信群聊机器人的url地址**、**钉钉群聊机器人的url地址**(在钉钉中创建时，验证方式选关键字，填入“签到”)、**Server酱的KEY**  
多账号时账号密码一行一个一一对应  
示例：  
**USER**
```
123456
24678
```
**PWD**
```
cxkjntm
jntmcxk
```

![](http://tu.yaohuo.me/imgs/2020/06/748bf9c0ca6143cd.png)
![](http://tu.yaohuo.me/imgs/2020/06/af2013b1ef5d8430.png)
![](http://tu.yaohuo.me/imgs/2020/06/09c22adcec7b5d81.png)


## 三、启用Action
1 点击**Action**，再点击**I understand my workflows, go ahead and enable them**  
2 修改任意文件后提交一次  
![](http://tu.yaohuo.me/imgs/2020/06/34ca160c972b9927.png)

## 四、查看运行结果
Actions > Cloud189Checkin > build  
能看到如下图所示，表示成功  
![](http://tu.yaohuo.me/imgs/2020/06/b9e596c99f3835e0.png)

此后，将会在每天9:01开始签到  
若有需求，可以在[.github/workflows/run.yml]中自行修改

## 可能遇到的问题
- 1. 验证码错误  
首先考虑是不是密码错误  
其次查看是否已经关闭设备锁  
- 2. 暂无

## 关于泄露手机号
本版本会打印手机号前3位与后4号，介意的请去py中修改：帐号下面那一行，前面加#号注释。  

## 关于签到结果通知
企业微信机器人、钉钉机器人、方糖Server酱，3个加一个就好了，当然你也可以不加或全加  
原peng4740的程序只是出错时通知，且是分别每个错通知，比较凌乱。现在改为不管签到成功还是出错，都会通知，这样也方便知道今天确实Action了，Github前些日子全改手动开启了，估计很多人都断签了。  

