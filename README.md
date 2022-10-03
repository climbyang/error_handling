# error_handling

## Case 1(案例一)：Use HBuilder with GitHub  
使用 HBuilder从Github clone source的时候遇到“鉴权失败”  

【error如下】  
cxxxx@MacBook-Pro miniprogram-xxxxxx % git clone https://github.com/cxxx/miniprogram-xxx.git  
正克隆到 'miniprogram-jiyun'...  
Username for 'https://github.com': cxxx@xxx.com  
Password for 'https://cxxx@xxx.com@github.com':   
remote: Support for password authentication was removed on August 13, 2021.  
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.  
fatal: 'https://github.com/cxxx/miniprogram-xxx.git/' 鉴权失败  
  
【解决方案】  
使用GitHub CLI，先安装如下  
Install:	brew install gh	 
Upgrade:  brew upgrade gh  
然后获取https登录验证：gh auth login  
验证后使用克隆source即可： gh repo clone cxxxx/miniprogram-xxx  
