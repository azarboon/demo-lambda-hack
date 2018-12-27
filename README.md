# Lambda hack demo

DO NOT USE THIS APPLICATION. IT'S VULNERABLE AND CAN PUT YOU IN RISK.

This is a demo hack that I used during my talk in DevOps 2018 conference. I'm publishing this for educational purpose. I will add link to talk's recording once it's ready. 



## Function logic

Once user sends message, applicaiton posts it on slack and saves it in dynamodb. 

## How it gets hacked?

This app is using vulnerable node-serialze library. It enables the attackers to inject their own command, and read (or even manipulate) dynamodb data.

## In action

Attacker injects his own command to zip Lambda folder, to encode and to send it to his own computer (I used ngrok. Ngrok assigns you a url and relays traffic into your local host). Once downloaded, attacker decodes and unzips folder, analyzes code and sends another request to query database.

In root folder, you can find Postman collection that has sample requests and codes.


## Acknowledgement

Thanks to Protego Labs for helping me with preparing this demo.

