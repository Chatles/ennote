# 结合Tar和OpenSSL给文件和目录加密及解密
https://www.cnblogs.com/kevingrace/p/8194784.html
```
//加密
tar -czf - * | openssl enc -e -aes256 -out note.tar.gz

//解密
openssl enc -d -aes256 -in note.tar.gz | tar xz -C 解压目录(默认当前目录)
```
