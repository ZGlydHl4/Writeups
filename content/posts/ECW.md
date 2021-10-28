+++
title = "ECW 2021"
date = "2021-10-27"
description = "European Cyber Week organized by \"Pôle d'Excellence CYBER\" and \"HOPSCOTCH CONGRÈS\""
tags = ["CTF", "Jeopardy"]
+++

# European Cyber Week

*From October 8th, 2021 to October 24th, 2021*

I granted 7 challenges over 22 :
  - [Response Team 1](#response-team-1)
  - [Response Team 2](#response-team-2)
  - [Nightly Planet 1](#nightly-planet-1)
  - [Nightly Planet 2](#nightly-planet-2)
  - [QRmedix](#qrmedix)
  - [Amovax](#amovax)
  - [Codiv Mafia](#codiv-mafia)

## Response Team 1



## Response Team 2



## Nightly Planet 1



## Nightly Planet 2



## QRmedix

> A vaccination campaign has gone wrong in Benin. Following the injection of the vaccine some people died.
>
> It is argued that there could have been a problem in the plant packaging the vaccine.
>  Only one box of this vaccine was found. A QRcode on the packaging has been preserved and internal sources told us that it is possible to find the number of the manufacturing site thanks to it.
>  However this does not seem to work with a traditional QRCode reader and you have been given the task of rebuilding it. You must silence the rumors about this vaccine as soon as possible!
>
>  For the validation of this challenge you must submit the identifier Usine (factory) as a flag.

Here is the QR code : 

![QR code](/images/QRcode_medics.png)

As we can see, 2 eyes are missing in the QR code. So we just have to modify the image with Gimp or Photoshop by adding these 2 eyes at the top right corner and the bottom left corner. 

![QR code complete](/images/QRcode_medics_complete.png)

Right after doing this we can use `zbar-tools` to retrieve informations from the QR code :

```bash
❯ zbarimg QRcode_medics_complete.png                    
QR-Code:Denomination=Comirnaty;ID_serie=287475322;Fabrication_date=23/05/2021;DLC=22/11/2021;ID_Usine=77ce347e6cee6e765aa3b006504b6bfa
scanned 1 barcode symbols from 1 images in 0,04 seconds
```

The flag is : `ECW{77ce347e6cee6e765aa3b006504b6bfa}`

## Amovax



## Codiv Mafia

