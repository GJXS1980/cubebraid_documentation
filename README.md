# 安装流程
## 依赖
python3.11
sphinx

## 项目配置流程
1. 创建新的虚拟环境
```bash
# 在CubeBraid Documentation目录下
py -3.11 -m venv cubebraiddoc

# 激活
ros2doc\Scripts\activate
```
2. 编译项目
```bash
# 安装依赖
python -m pip install -r requirements.txt -c constraints.txt

# 编译
python -m sphinx -b html -c . source build\html

# 启动
python -m http.server 8000 --directory build\html

# 浏览器访问 http://localhost:8000
```

3. 设置开机自启动(ubuntu)
```bash
# 创建 systemd 服务
sudo gedit /etc/systemd/system/cubebraiddoc.service
```
cubebraiddoc.service文件内容如下：
```bash
[Unit]
Description=CubeBraid Documentation HTTP Server
After=network.target

[Service]
Type=simple
User=hgrd
WorkingDirectory=/home/hgrd/demo/cubebraid_documentation
ExecStart=/home/hgrd/demo/cubebraid_documentation/cubebraiddoc/bin/python -m http.server 8000 --bind 0.0.0.0 --directory /home/hgrd/demo/cubebraid_documentation/build/html
Restart=always
RestartSec=5

[Install]
WantedBy=multi-user.target
```

环境配置：
```bash
# 让 systemd 重新读取配置
sudo systemctl daemon-reload

# 设置开机自动启动
sudo systemctl enable cubebraiddoc.service

# 立即启动
sudo systemctl start cubebraiddoc.service

# 检查服务状态
sudo systemctl status cubebraiddoc.service

# 浏览器访问
http://localhost:8000
```
