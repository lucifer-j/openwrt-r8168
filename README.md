# openwrt-lede
https://github.com/coolsnowwolf/lede
# openwrt-r8168
Realtek RTL8168 Driver for Openwrt
方法：
```bash
cd package
git clone https://github.com/lucifer-j/openwrt-r8168
cd ..
```
# 插件仓库
https://github.com/liuran001/openwrt-packages

# 修改默认IP
```bash
cd lede
vim package/base-files/files/bin/config_generate
```
![image](https://user-images.githubusercontent.com/4360479/164149693-78b9800e-5051-4297-8779-6e4a78ecdbc3.png)

# 添加DNS和网关IP
```bash
set network.$1.gateway='192.168.1.1'
set network.$1.dns='127.0.0.1 223.5.5.5 8.8.8.8'
```
第一个是网关的地址，第二个是DNS地址，可以设置多个DNS地址中间用空格隔开。
![image](https://user-images.githubusercontent.com/4360479/164149799-be6e3b09-55bd-4f16-9236-ee3dddf9e338.png)
保存退出，删除临时文件夹，终端输入：
```bash
rm -rf tmp
```
