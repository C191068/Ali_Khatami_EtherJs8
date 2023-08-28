![image](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/ad6a4cdd-6bdc-4739-a15f-5b11065593cd)# Ali_Khatami_Etherjs8(Learning from the video of Patrick Collins)

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

![m15](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/8f7013ab-4863-4efe-a98a-dc986c92a132)
we can see here encrypted key <br>

![m16](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/753fd7f5-88c3-4385-8810-0ad2ab548063)

In gitignore we add .encryptedKey.json <br>

![m17](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/b2efa71e-27a0-49b7-8725-c31dd34b1d37)

We have remove the private key and privete_key_password form the above .env file  <br>

So that password is not hanging around in plain text <br>


Now in our deploy script we can change the way we actually get the wallet <br>

![m18](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/361950b5-5559-4375-af4e-7bc288d21327)

we are getting the wallet by passing the private key like the above <br>

But we are not gonna do this <br>

We gonna use our encrypted key that we just created <br>

![m19](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/aacc0ce9-b8f9-4ecf-bf6e-19f0e1968269)

For that we use the above line of code <br>

The above ```fs.readFileSync``` is gonna read from ```encryptedKey.json``` into this ```const encryptedJson``` <br>

![m22](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/050b3291-204b-42e8-b7cf-9e62a1a2214f)


now we gonna create a wallet from this encrypted key in the above way <br>

Here in the above we pass the encrypted.json file and the password 

 the resaon we use let in the above becaues we have to connect this wallet <br>
 back to our provider <br>

 
 If we look at the above mentioned arrow we are not connecting our wallet <br>
 back to our provider <br>


![m21](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/2e3644ae-0930-408f-a8d1-09e788bb2ff2)

 For that we use the above line of code <br>

 
Now if we run our akrkdeploy.js with our private key password <br>

as an environment variable it should still deploy  <br>


![m23](https://github.com/C191068/Ali_Khatami_EtherJs8/assets/89090776/ef15b075-1908-4826-a0f5-3462c88a17b4)

We have corrected at let wallet part shown with white arrow <br>
thus we have sucessfully deployed shown with yeloow arrow <br>



















 






