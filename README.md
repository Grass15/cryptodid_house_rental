
# Rental Merchant Website

## Description 
This use case demonstrates the effectiveness of the MG FHE protocol in a scenario where a financial transaction is <br> required. In this example, a user wants to rent a house through an online web application. Using his digital wallet, <br> the user gets his personal information verified without the website having to interact with it directly.

## Preview 

The user is looking to rent a home on this web application.
<br>

<img src= homepage.png alt ="Home page" width = "800" height = "450">

*After picking a house and fetching the necessary claims,*

<img src= almostverified.png alt ="information required" width = "800" height = "450">

*the user can click on Fill and Verify to scan the QR code.*

<img src= verified.png alt ="Successfully approved" width = "800" height = "450">

<br>

## Setup
To execute the demonstration, you will need the following tools pre-installed:
- [Node.js](https://nodejs.org/en/download) (intall npm with node.js) 
- [cryptodid_verifier](https://github.com/Grass15/cryptodid_verifier.git) 
- [cryptodid_android_app](https://github.com/Grass15/cryptodid_android_app)
- [Git](https://git-scm.com/download)

## Install & Run

1. Open a new shell
2. Copy the repository to your machine
```terminal
git clone https://github.com/Grass15/cryptodid_house_rental.git
```
3. Install packages 
```terminal
cd cryptodid_house_rental
npm install
```
4. Start the web application 
```terminal 
npm start
```

<br>

&nbsp; To execute the full demonstration, follow the next steps:

<br>

5. Access to cryptodid_verifier\src\Housing\ApplicationPage.js 
<br>
  
&nbsp;  Change the line:
  
      const ws = new WebSocket("wss://cryptodid.herokuapp.com/verify")
&nbsp;  With: 
  
      const ws = new WebSocket("ws://yourverifierIp:yourVerifierPort/verify")
&nbsp;  Example: 
  
      const ws = new WebSocket("ws://192.168.1.14:8080/verify")
    
&nbsp;   Change the line: 
   
      <QRCode value={"cryptodid.herokuapp.com"} />
&nbsp;   With: 
   
      <QRCode value={"yourverifierIp:yourVerifierPort"} />
&nbsp;   Example: 
   
      <QRCode value={"192.168.1.14:8080"} />
  
6. Execute the cryptodid_verifier <br>
  
7. Execute the cryptodid_android_app (make sure your android device is paired)
  
8. Fetch the necessary claims and click on "Verify a Claim" to scan the QR code


