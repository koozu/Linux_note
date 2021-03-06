# Docker
- [Centos7 利用 docker 在觀看 youtube 時不受廣告干擾](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W1-20200915.md)
- [Docker](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md)
    - [Docker 介紹](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#docker-%E4%BB%8B%E7%B4%B9)
    - [Docker 使用](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#docker-%E4%BD%BF%E7%94%A8)
    - [容器與虛擬機器](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E5%AE%B9%E5%99%A8%E8%88%87%E8%99%9B%E6%93%AC%E6%A9%9F%E5%99%A8)
        - [容器](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E5%AE%B9%E5%99%A8)
        - [虛擬機](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E8%99%9B%E6%93%AC%E6%A9%9F)
    - [Docker 特色](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#docker-%E7%89%B9%E8%89%B2)
        - [LXC 命名空間隔離](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#1-lxc-%E5%91%BD%E5%90%8D%E7%A9%BA%E9%96%93%E9%9A%94%E9%9B%A2)
        - [aufs(advanced multi-layered unification filesystem) 架構](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#2-aufsadvanced-multi-layered-unification-filesystem-%E6%9E%B6%E6%A7%8B)
    - [鏡像/映象檔(Image) 與 容器(Container)](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E9%8F%A1%E5%83%8F%E6%98%A0%E8%B1%A1%E6%AA%94image-%E8%88%87-%E5%AE%B9%E5%99%A8container)
    - [安裝 Docker](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E5%AE%89%E8%A3%9D-docker)
    - [Docker 指令](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#docker-%E6%8C%87%E4%BB%A4)
    - [補充：遇到無法安裝 Centos7 Docker](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E8%A3%9C%E5%85%85%E9%81%87%E5%88%B0%E7%84%A1%E6%B3%95%E5%AE%89%E8%A3%9D-centos7-docker)
    - [安裝 Docker-compose](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W2-20200922.md#%E5%AE%89%E8%A3%9D-docker-compose)
- [Docker 實作](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#docker-%E5%AF%A6%E4%BD%9C)
    - [busybox](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#busybox)
        - [安裝 busybox](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#%E5%AE%89%E8%A3%9D-busybox)
        - [一次性指令](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#%E4%B8%80%E6%AC%A1%E6%80%A7%E6%8C%87%E4%BB%A4)
    - [使用容器環境](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#%E4%BD%BF%E7%94%A8%E5%AE%B9%E5%99%A8%E7%92%B0%E5%A2%83)
        - [C](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#c)
        - [Python](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#python)
        - [Httpd](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#httpd)
            1. [將虛擬機的資料夾映射到 docker 環境中](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#1%E5%B0%87%E8%99%9B%E6%93%AC%E6%A9%9F%E7%9A%84%E8%B3%87%E6%96%99%E5%A4%BE%E6%98%A0%E5%B0%84%E5%88%B0-docker-%E7%92%B0%E5%A2%83%E4%B8%AD)
            2. [利用`docker cp`將虛擬機的資料夾映射到 docker 環境中](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W3-20200929.md#2%E5%88%A9%E7%94%A8docker-cp%E5%B0%87%E8%99%9B%E6%93%AC%E6%A9%9F%E7%9A%84%E8%B3%87%E6%96%99%E5%A4%BE%E6%98%A0%E5%B0%84%E5%88%B0-docker-%E7%92%B0%E5%A2%83%E4%B8%AD)
    - [將資料從第一台(192.168.56.101)傳到第二台機器(192.168.56.102)](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#%E5%B0%87%E8%B3%87%E6%96%99%E5%BE%9E%E7%AC%AC%E4%B8%80%E5%8F%B019216856101%E5%82%B3%E5%88%B0%E7%AC%AC%E4%BA%8C%E5%8F%B0%E6%A9%9F%E5%99%A819216856102)
    - [查看 docker 容器使用的資源](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#%E6%9F%A5%E7%9C%8B-docker-%E5%AE%B9%E5%99%A8%E4%BD%BF%E7%94%A8%E7%9A%84%E8%B3%87%E6%BA%90)
    - [Harbor 私有倉儲](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#harbor-%E7%A7%81%E6%9C%89%E5%80%89%E5%84%B2)
        - [安裝 docker harbor](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#%E5%AE%89%E8%A3%9D-docker-harbor)
        - [上傳鏡像檔至 Harbor](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#%E4%B8%8A%E5%82%B3%E9%8F%A1%E5%83%8F%E6%AA%94%E8%87%B3-harbor)
- [Docker Network](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#docker-network)
    - [none network：在啟動 docker 的時候，不要開啟任何網路](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#none-network%E5%9C%A8%E5%95%9F%E5%8B%95-docker-%E7%9A%84%E6%99%82%E5%80%99%E4%B8%8D%E8%A6%81%E9%96%8B%E5%95%9F%E4%BB%BB%E4%BD%95%E7%B6%B2%E8%B7%AF)
    - [host network：docker 的網路和 host 網路一樣](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#host-networkdocker-%E7%9A%84%E7%B6%B2%E8%B7%AF%E5%92%8C-host-%E7%B6%B2%E8%B7%AF%E4%B8%80%E6%A8%A3)
    - [bridge network：橋接網路，預設的網路 (docker 0)](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W4-20201006.md#bridge-network%E6%A9%8B%E6%8E%A5%E7%B6%B2%E8%B7%AF%E9%A0%90%E8%A8%AD%E7%9A%84%E7%B6%B2%E8%B7%AF-docker-0)
    - [容器互連（linking）](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#%E5%AE%B9%E5%99%A8%E4%BA%92%E9%80%A3linking)
    - [使用自訂的 bridge Network](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#%E4%BD%BF%E7%94%A8%E8%87%AA%E8%A8%82%E7%9A%84-bridge-network)
    - [資料卷 Data Volume](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#%E8%B3%87%E6%96%99%E5%8D%B7-data-volume)
        - [A. 將本機端資料夾掛載在 Docker 的網頁伺服器](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#a-%E5%B0%87%E6%9C%AC%E6%A9%9F%E7%AB%AF%E8%B3%87%E6%96%99%E5%A4%BE%E6%8E%9B%E8%BC%89%E5%9C%A8-docker-%E7%9A%84%E7%B6%B2%E9%A0%81%E4%BC%BA%E6%9C%8D%E5%99%A8)
        - [B. 沒有名稱的 Data Volume](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#b-%E6%B2%92%E6%9C%89%E5%90%8D%E7%A8%B1%E7%9A%84-data-volume)
        - [C. 有名稱的 Data Volume](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#c-%E6%9C%89%E5%90%8D%E7%A8%B1%E7%9A%84-data-volume)
* [Portainer - 圖形化介面管理 docker](https://github.com/linjiachi/Linux_note/blob/master/109-1%20Docker/W5-20201013.md#portainer---%E5%9C%96%E5%BD%A2%E5%8C%96%E4%BB%8B%E9%9D%A2%E7%AE%A1%E7%90%86-docker)