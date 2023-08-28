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





 
 


 






