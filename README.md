<div align="center">
  <a href="https://rustvnt.com">
<img src="https://socialify.git.ci/vnt-dev/vnt/image?description=1&logo=https%3A%2F%2Fraw.githubusercontent.com%2Fvnt-dev%2FVntApp%2Fmaster%2Fandroid%2Fapp%2Fsrc%2Fmain%2Fres%2Fmipmap-xxxhdpi%2Fic_launcher.png&name=1&pattern=Plus&theme=Auto" alt="" width="640" height="320" /></a>
<div>
  <img src="https://hits.5670567.xyz/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Flmq8267%2Fvnt_fpk&count_bg=%2379C83D&title_bg=%23555555&icon=github.svg&icon_color=%23F6F6F6&title=%E8%AE%BF%E9%97%AE%E7%BB%9F%E8%AE%A1&edge_flat=false"/>
	<h1>VNT - 飞牛fpk安装包</h1>
</div>
</div>

- 支持 `x86_64` `arm64` `arm` `armv7`  `i386`等架构，下载后在应用商店 手动上传安装即可，理论是支持所有架构的飞牛NAS安装的。

- `*_all.fpk`是新版本自动识别架构的安装包 `*_x86.spk` `*_arm.spk` 是旧版本无法识别全架构的安装包

- 首次安装客户端，安装完成后需要打开客户端进去填写配置文件再启动。

- 服务端配置在安装时配置，后续需要修改 在 应用设置 修改后重启应用生效，数据文件和日志在 文件管理 - 应用文件里。

- 群晖的在[lmq8267/vnt_dsm](https://github.com/lmq8267/vnt_dsm) ,在线配置文件[生成](https://lmq8267.github.io/VNT-Magisk/)

**如果你需要在外面通过手机端来访问飞牛局域网内的其他设备（如：电脑、路由器等）无法访问时：**

- 确保你的飞牛配置文件填写了 `out_ips:` 参数，对应飞牛的局域网网段 例如`192.168.1.0/24` 并且关闭了 内置IP代理参数 `no_proxy: true`
- 确保你的手机app端配置了 `in-ip` 飞牛的局域网网段,飞牛的虚拟ip，例如 `192.168.1.0/24,10.26.0.2`
- 去掉[vnt/cmd/main](https://github.com/lmq8267/vnt_fpk/blob/a3eb232b13fe927008b66511a0c16c1780882f9b/vnt/cmd/main#L125)中的 # 使其生效，已经安装的话对应目录里`/var/apps/vnt/cmd/main` 修改即可  
  <img width="942" height="157" alt="image" src="https://github.com/user-attachments/assets/35c715fe-31da-4e15-bb60-450c23e514d4" />
  其中`10.26.0.0/24`对应你组网的虚拟网段，我没有添加是因为如果你自建服务器的话 改变了虚拟网段不是10.26.0.0/24就无效了

- 如还是无法访问 考虑 在上方命令后追加一行 `sysctl -w net.ipv4.ip_forward=1`

## UI预览

### VNT客户端

<img width="1506" height="794" alt="G8TO3UOT9}6 {LELW)2SAK" src="https://github.com/user-attachments/assets/09207a5e-5544-47f4-a0af-fec49c494ced" />

<img width="1423" height="684" alt="image" src="https://github.com/user-attachments/assets/3507deb0-23fd-4382-a784-1c0836ce445e" />

<img width="1436" height="767" alt="image" src="https://github.com/user-attachments/assets/ec8dbdcb-d82f-4f70-a651-0332c0a7ffad" />

### VNTS服务端

<img width="1413" height="800" alt="image" src="https://github.com/user-attachments/assets/fd401e38-5389-4c4d-a120-400cc1c24283" />

<img width="963" height="657" alt="image" src="https://github.com/user-attachments/assets/174c2cc5-561c-4ca2-99c4-b1bbe8a725a7" />

