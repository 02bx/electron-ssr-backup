# 收集已知问题和解决方案

## Archlinux or Manjaro 无法运行的问题解决
Manjaro/Archlinux 运行程序时无法运行，在终端运行 electron-ssr 发现缺少 lib-gconf.so 这个库文件，只需要安装 gconf 即可解决
`sudo pacman -S gconf`

### Manjaro无法代理（其他linux可以参考）
一、PAC模式不可用
安装proxychains，可从软件仓库安装或[github](https://github.com/rofl0r/proxychains-ng.git)
``` bash
sudo vi /etc/proxychains.conf
```
将socks4 127.0.0.1 9095改为
```bash
socks5 127.0.0.1 1080
```
重启服务
