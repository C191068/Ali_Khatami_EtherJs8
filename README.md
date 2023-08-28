# Ali_Khatami_Etherjs8(Learning from the video of Patrick Collins)

### Better private Key Management

For example if we feel nervous to put private key to .env file <br>
thinking that we accidentally push it to github <br>
So what we can do we can add private key in our RPC URL <br>

as our environment variables right in the command line <br>

If we use it in our .env file we can encrypt it  <br>
 and store our encrypted key locally <br>

 Now in that way if somebody does get into our account <br>

 our private key is not sitting in plain text <br>
 It is encrypted and to decrypt it requires password <br>

 which only we know <br>

 ![m6](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/e9b27549-28c1-4ef7-a9b1-0c093fe2a4ea)

For that we create a new file like the above <br>

here we actually use some code to encrypt the private key <br>



![m7](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/b257b89f-1b73-40a7-87ae-37e8e0420fc6)

 So we gonna set this script to run our encrypt key one time <br>
 And they we gonna remove our private form anywhere in workspace <br>
 So that it is no longer in plaintext anywhere <br>

 ![m8](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/a09e9fa2-217e-4ea3-bfa1-e04bc991e109)

here we created a new wallet which is new but different <br>
We do need a private key to stick in here <br>


![m9](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/06c5b07f-a772-4e7d-95cb-3bbeb3058033)

Thsi encypt function gonna return encryptedJsonKey <br>
that we can store locally and can can only decrypt it <br>
with password <br>

It takes two parameter one is PRIVATEKEY and another 9is PRIVATE_KEY password <br>

![m10](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/6ab455b5-7212-4630-ad24-df41af68063d)

here we created a password at .env file <br>

![m11](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/2f06bca1-0aa4-461f-ae23-fd7b650261eb)


Thus we have made changes in the above <br>

![m12](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/6c28bcdb-6150-43fa-84a3-439d449e5e2c)

Thus we run our code <br>

these Json object shown with yellow arrow is what our key looks like encrypted  <br>

In order everything in the above like address, id are all the encrypted  version of the key <br>

if somebody gets into aour account and see the above they will have <br>
to know the password to decypt these json object back into private key <br>


![m13](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/f3ab5f06-36bd-4e17-8e0c-f84e63758432)

We are saving it to a new file ```.encryptedKey.json``` and we are passing it this <br>
encrypted key i.e encryptedJsonKey that we just made <br>


![m14](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/f63efacd-05be-43ed-a03f-d5b348759806)

Now we run the code at console shown with white arrow we see a new file .encryptedKey.json shown with <br>
yellow arrow is created <br>







 
 


 






