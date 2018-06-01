# AES-
aes传输数据加密

AES传输数据加密方式
1. aes加密需要key和iv,协商秘钥和偏移量
var key = CryptoJS.enc.Utf8.parse("8IudzhuLuzWfpZGq");
var iv = CryptoJS.enc.Utf8.parse('1234567890123456');
2. 加密顺序: utf-8编码,AES加密方封装方法进行加密,base64编码,(如有需要: 去除特殊字符传递丢失,需encodeURIComponent()再次编码)
3. aes加密,只能加密字符串,so..无论加密还是解密,数据类型应该是string
4. aes解密,直接使用AES封装方法解密,注意:获得解密后的数据为字符串,JSON.parse(),转换获得object
