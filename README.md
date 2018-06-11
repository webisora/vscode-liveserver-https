# vscode-liveserver-https
How to enable HTTPS protocol on live server Visual Code

First you will need a self-signed SSL Certificate. If you don’t know how to create a self-signed SSL Certificate goto https://www.akadia.com/services/ssh_test_certificate.html and follow the steps.
[Note: If you are using Visual Code in windows, download OpenSSL and continue the process.]

After you have the private key and certificate:

- Go to your visual code project.
- Create ```.vscode``` folder inside the project. ( Don’t forget the . (period) ).
- Inside that folder create ```settings.json``` file.
- Paste the following code:

  ```json
  {  
  "liveServer.settings.https":   
  {
  "enable": true, //set it true to enable the feature.  
  "cert": "D:\\https\\primary.crt", //full path of the certificate  
  "key": "D:\\https\\private.key", //full path of the private key  
  "passphrase": "12345"  
  }  
  }
  ```
  
- Start the Live Server and access your project using HTTPS
