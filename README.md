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

```html
<script type="text/javascript">
    //实例化一个对象，包含全部操作，可传入秘钥长度和指数作为参数
    var encrypt = new JSEncrypt();
    //若没有秘钥可用该函数自动生成一对秘钥
    encrypt.getKey();
    //分别返回私钥和公钥，pem格式
    encrypt.getPrivateKey();
    encrypt.getPublicKey();
    //分别返回私钥和公钥，字符串格式
    encrypt.getPrivateKeyB64();
    encrypt.getPublicKeyB64();
    //如果有秘钥，可以用一下函数自己设置秘钥
    encrypt.setKey(); //传入秘钥对象或字符串
    encrypt.setPrivateKey(); //传入字符串
    encrypt.setPublicKey();  //传入字符串
    //解析秘钥对，可以将秘钥中的指数与系数分解出来，有特殊需要的可以使用
    encrypt.key.parseKey();
    //加密，返回经过BASE64编码的密文
    encrypt.encrypt(str);
</script>
  
```
