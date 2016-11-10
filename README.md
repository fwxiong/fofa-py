# FOFA Pro SDK 使用说明文档
## FOFA Pro API   
<a href="https://fofa.so/api"><font face="menlo">`FOFA Pro API`</font></a> 是资产搜索引擎 <a href="https://fofa.so/">`FOFA Pro`</a> 为开发者提供的 `RESTful API` 接口, 允许开发者在自己的项目中集成 `FOFA Pro` 的功能。    


## FOFA SDK
基于 `FOFA Pro API` 编写的 `python` 版 `SDK`, 方便 `python` 开发者快速将 `FOFA Pro` 集成到自己的项目中。


## 环境
### 开发环境
``` 
windows7 + Python 2.7.10 + pycharm 2016.2.3
```
### 测试环境
``` 
Ubuntu 16.04 LTS x64 +  Python 2.7.12
```
### 使用环境
`Python 2.x`   

## 获取
### `pip`
安装 `FOFA SDK` 之前，请先确认已经安装 <a href="https://pypi.python.org/pypi/pip/"><font face="menlo">pip</font></a>.   

`点击`  <a href="https://pip.pypa.io/en/stable/"><font face="menlo">pip documentation</font></a> `了解详细的说明`      


### FOFA SDK

<strong>安装</strong>  
```
pip install fofa
```

## 依赖
### Email & API Key   
| `Email` |用户登陆 `FOFA Pro` 使用的 `Email`|
|---------|:-----------------:|
|`Key`| 前往 <a href="https://fofa.so/my/users/info" style="color:#0000ff"><strong>`个人中心`</strong></a> 查看 `API Key` 


## Example   
``` python
# -*- coding: utf-8 -*-
import fofa

if __name__ == "__main__":
    email, key = ('test@test.com','xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx')
    client = fofa.Client(email, key)
    data = client.get_data('''host="fofa.so"''',fields="ip,city")
    for ip,city in data["results"]:
        print "%s,%s"%(ip,city)
```

## 协议
`FOFA SDK` 遵循 `BSD` 协议 <a href="https://opensource.org/licenses/BSD-3-Clause">https://opensource.org/licenses/BSD-3-Clause</a>