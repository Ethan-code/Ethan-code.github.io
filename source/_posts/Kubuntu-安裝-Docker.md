---
title: Kubuntu 安裝 Docker
date: 2022-01-18 21:07:17
tags:
- kubuntu
- docker
---

## 步驟
1. 安裝相關套件：`sudo apt-get install ca-certificates curl gnupg lsb-release`
2. 加入 Docker GPG key：`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`
3. 設定 stable repository：`echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
4. 更新 package 清單並安裝
  ```bash
    sudo apt-get update
    sudo apt-get install docker-ce docker-ce-cli containerd.io
  ```
5. 測試是否安裝成功：`sudo docker run hello-world`
  - 預設 linux 都會要求管理員權限來執行
  - 如果不想使用 `sudo` 需要建立群組並將當前使用者加入群組（登出才會生效）
    ```bash
    sudo groupadd docker
    sudo usermod -aG docker $USER
    ```

## 參考資料
- [Install Docker Engine on Ubuntu | Docker Documentation](https://docs.docker.com/engine/install/ubuntu/)
