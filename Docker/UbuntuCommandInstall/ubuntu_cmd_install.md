# Dockerで遊んでいたら…
 Docker内でubuntuを対話モードで色々なコマンドを試してみようとしたところ、
 **nslookup**や**curl**が入ってない(未インストール)というエラーが発生したため、
 とりあえずコマンドをインストールする方法をメモとして残しておく.
1. nslookup
コマンドラインで`apt-get install dnsutils`を実行する.  
以下実行結果の例  
`root@999999999999:/# apt-get install dnsutils  
Reading package lists... Done  
Building dependency tree  
Reading state information... Done  
The following additional packages will be installed:  
  bind9-host geoip-database krb5-locales libbind9-160 libdns1100 libgeoip1 libgssapi-krb5-2 libicu60 libirs160 libisc169 libisccc160   libisccfg160 libjson-c3 libk5crypto3 libkeyutils1  
  libkrb5-3 libkrb5support0 liblwres160 libssl1.1 libxml2  
Suggested packages:  
  rblcheck geoip-bin krb5-doc krb5-user  
The following NEW packages will be installed:  
  bind9-host dnsutils geoip-database krb5-locales libbind9-160 libdns1100 libgeoip1 libgssapi-krb5-2 libicu60 libirs160 libisc169   libisccc160 libisccfg160 libjson-c3 libk5crypto3 libkeyutils1  
  libkrb5-3 libkrb5support0 liblwres160 libssl1.1 libxml2  
0 upgraded, 21 newly installed, 0 to remove and 16 not upgraded.  
Need to get 14.3 MB of archives.  
After this operation, 54.5 MB of additional disk space will be used.  
Do you want to continue? [Y/n] y  
Get:1 http://archive.ubuntu.com/ubuntu bionic-updates/main amd64 libicu60 amd64 60.2-3ubuntu3.1 [8054 kB]  
Get:2 http://archive.ubuntu.com/ubuntu bionic-updates/main amd64 libjson-c3 amd64 0.12.1-1.3ubuntu0.3 [21.7 kB]  
Get:3 http://archive.ubuntu.com/ubuntu bionic-updates/main amd64 libssl1.1 amd64 1.1.1-1ubuntu2.1~18.04.6 [1301 kB]  
～略～  
Setting up libbind9-160:amd64 (1:9.11.3+dfsg-1ubuntu1.12) ...  
Setting up bind9-host (1:9.11.3+dfsg-1ubuntu1.12) ...  
Setting up dnsutils (1:9.11.3+dfsg-1ubuntu1.12) ...  
Processing triggers for libc-bin (2.27-3ubuntu1) ...`
1. curl
コマンドラインで`apt-get install curl`を実行する.  
以下実行結果の例  
`root@999999999999:/# apt-get install curl  
Reading package lists... Done  
Building dependency tree  
Reading state information... Done  
The following additional packages will be installed:  
  ca-certificates libasn1-8-heimdal libcurl4 libgssapi3-heimdal libhcrypto4-heimdal libheimbase1-heimdal libheimntlm0-heimdal libhx509-5-heimdal libkrb5-26-heimdal libldap-2.4-2  
  libldap-common libnghttp2-14 libpsl5 libroken18-heimdal librtmp1 libsasl2-2 libsasl2-modules libsasl2-modules-db libsqlite3-0   libwind0-heimdal openssl publicsuffix  
Suggested packages:  
  libsasl2-modules-gssapi-mit | libsasl2-modules-gssapi-heimdal libsasl2-modules-ldap libsasl2-modules-otp libsasl2-modules-sql
The following NEW packages will be installed:  
  ca-certificates curl libasn1-8-heimdal libcurl4 libgssapi3-heimdal libhcrypto4-heimdal libheimbase1-heimdal libheimntlm0-heimdal libhx509-5-heimdal libkrb5-26-heimdal libldap-2.4-2  
  libldap-common libnghttp2-14 libpsl5 libroken18-heimdal librtmp1 libsasl2-2 libsasl2-modules libsasl2-modules-db libsqlite3-0 libwind0-heimdal openssl publicsuffix  
0 upgraded, 23 newly installed, 0 to remove and 16 not upgraded.  
Need to get 2996 kB of archives.  
After this operation, 8610 kB of additional disk space will be used.  
Do you want to continue? [Y/n] y  
Get:1 http://archive.ubuntu.com/ubuntu bionic-updates/main amd64 openssl amd64 1.1.1-1ubuntu2.1~18.04.6 [614 kB]  
Get:2 http://archive.ubuntu.com/ubuntu bionic/main amd64 ca-certificates all 20180409 [151 kB]  
～略～  
Processing triggers for ca-certificates (20180409) ...  
Updating certificates in /etc/ssl/certs...  
0 added, 0 removed; done.  
Running hooks in /etc/ca-certificates/update.d...  
done.`

> # 参考
> [410gone](https://410gone.click/blog/ubuntu-dig-nslookup-nsupdate%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B/)
> [あんらぶぎーくどっとこむ](https://410gone.click/blog/ubuntu-dig-nslookup-nsupdate%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B/)
