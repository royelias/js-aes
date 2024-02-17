# js-aes
perform AES encryption and decryption. zero dependencies, only javascript used, designed mainly to handle AES encryption for payment systems. 


### install
```
npm i js-aes;
```
### JS_AES Incluse 
```  AESEncrypt, AESDencrypt, AESEncryptHex, AESDencryptHex  ```
### Parameters
1. data : data to be encrypted or decrypted. 
2. key  : the secret used to encrypt or decrypt.
3. operation : use keywords 'encrypt' or 'decrypt', 
4. mode  : cbc or ecb 
5. padding : use value "1" or "2" 
6. iv : default value '00000000000000000000000000000000' but you can use and share anothet value.

### Examples Usage
#### using hexadecimal values for data and Key
no conversion will be done on key and data
```
const jsaes = require('js-aes');
console.log( jsaes.AESEncryptHex('746573742064617461','7465737420646174617465737420646174657374206461746174657374206461','encrypt','cbc', '1','00000000000000000000000000000000') );
```
#### using ascii values for data.
convert to hexadecimal then do the AES operations.
```
const jsaes = require('js-aes');
console.log( jsaes.AESEncrypt('test data','7465737420646174617465737420646174657374206461746174657374206461','encrypt','cbc', '1','00000000000000000000000000000000') );
```
