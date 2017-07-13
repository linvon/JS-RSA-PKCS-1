# JS-RSA-PKCS-1
A demo for RSA encrypt/decrypt with JSEncrypt

JS内容来自于[JSEncrypt](https://github.com/travist/jsencrypt)  
因为原内容是英文撰写，这边做一个简单的中文Demo，方便查阅  
<hr>
首先说明一下，这个库文件在原仓库中有提供源码，各类demo，以及压缩后的min.js，方便开发使用  
全部采用原生JS完成，加密方式采用RSA PKCS#1 v1.5 padding，与OpenSSL默认加解密方式相同，可以通用。  
OpenSSL相关命令操作可以查看原仓库内容，不再赘述。
<hr>
原生实现内容在example.html中有展示，这边做一个简单的解释。  
`var encrypt = new JSEncrypt();  
    encrypt.getKey(); `