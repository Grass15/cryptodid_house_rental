# Rental Merchant Website
  
  Guide to setup on your local machine
  
  Prerequistes: 

    Nodejs and NPM

  To run the project, after cloning the project in the project directory, you can run:
  
  ### `npm install`
  ### `npm start`
  
  If you setup the verifier on your local machine do the following changes:
  
  Access to src\Housing\ApplicationPage.js
  
  Change the line:
  
      const ws = new WebSocket("wss://cryptodid.herokuapp.com/verify")
  With: 
  
      const ws = new WebSocket("ws://yourverifierIp:yourVerifierPort/verify")
  Example: 
  
      const ws = new WebSocket("ws://192.168.1.14:8080/verify")
    
   Change the line: 
   
      <QRCode value={"cryptodid.herokuapp.com"} />
   With: 
   
      <QRCode value={"yourverifierIp:yourVerifierPort"} />
   Example: 
   
      <QRCode value={"192.168.1.14:8080"} />
  


