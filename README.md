useradd zowe --shell /bin/bash --create-home
echo zowe:zowe | chpasswd
usermod -aG sudo zowe
echo "cd ~" >> ${bashEnv} && echo "cd ~" >> /home/zowe/.bashrc
su zowe
