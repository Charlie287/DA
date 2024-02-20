```
apt-get update
apt-get upgrade
python3 -m pip install --user ansible
pip install paramiko
pip install ansible-pylibssh
```

### Mở tập tin cấu hình với trình soạn thảo văn bản, ví dụ:
	`nano ~/.bashrc`
### Thêm dòng sau vào cuối tập tin:
	`export PATH=$PATH:~/.local/bin`
### Lưu tập tin và tái tải cấu hình:
	`source ~/.bashrc`

`ansible-galaxy collection install cisco.ios`
