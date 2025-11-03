## X

### Pyramid of pain

The pyramid of pain is the visual chart of how timeconsuming it is for the attacker when the defender reacts to different levels of indicators. The higher the more "painfull".

<img width="842" height="546" alt="image" src="https://github.com/user-attachments/assets/6d479273-b1b3-4ce4-8b23-ab0e5407f879" />

source: https://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html

### The diamond model

The diamond model is a way of analyzing a cyberattack to get a wholistic view. You applie it att all stages of for example the killchain and enshure that atleast one part of the model gets filled at each stage.

<img width="1582" height="972" alt="image" src="https://github.com/user-attachments/assets/30a8d9d0-b40b-43a6-b1f8-9bbc01cc04fa" />

source: https://www.youtube.com/watch?v=w8mEG52tfsY&t=1053s

## A
```$ ```
First i ran ```$ sudo apt-get update``` to ensure everything is up to date

Then i ran ```$ sudo apt install apache2``` to install apache 2

Then we start and enable apache2

<img width="949" height="86" alt="image" src="https://github.com/user-attachments/assets/e592533b-5611-4224-bfd7-6ecf5a853b7a" />

Afther this i checked it's status and got an error. I decided to try it anyways and as you might expect the default webpage didn't load.

<img width="2444" height="1069" alt="image" src="https://github.com/user-attachments/assets/2e272202-a5bf-4672-86cb-1ce73f1e885c" />

Afther some googling this could be due to it being blocked by the firewall. so i tried allowing port 80 over tcp

<img width="801" height="214" alt="image" src="https://github.com/user-attachments/assets/075bd9d0-bdfa-4e45-8e80-f324cd408ddb" />

tried restarting apache, no change, same error.

Tried redoing a couple steps and tried to account for human error. Turns out i am stupid and typed https instead of http. problem solved.

<img width="1611" height="1487" alt="image" src="https://github.com/user-attachments/assets/af326677-9569-4588-9b2e-62d2da4bd2b9" />

## B Nmapped

First i verified nmap was up to date

<img width="2380" height="446" alt="image" src="https://github.com/user-attachments/assets/2eba3698-b005-4c73-9a14-dfffe650195c" />

next i turned of my internet connection on the host device as it is easyer an safer.

After i did this i scanned localhost port 80.

<img width="2028" height="745" alt="image" src="https://github.com/user-attachments/assets/00886fc4-daa7-4056-b975-4d5c329add2d" />

The scan shows that the Apache HTTP server is upp and running.

## C Scripts

As can be seen in exersice B we have HTTP-Server-Header and HTTP-Title for the apache server.

## D

first i checked the recent logs. 

<img width="2463" height="1400" alt="image" src="https://github.com/user-attachments/assets/70d9d178-4d00-47d2-a679-77b4310991e9" />

Then i narrowed the search a bit to just nmap

<img width="2458" height="1418" alt="image" src="https://github.com/user-attachments/assets/bdaed100-485f-4858-a6c8-574da434bd4f" />

To explain the code above, i used grep to search trough the loggs for only entries containing the string "nmap" and the -i made the search case insensitive.

## E

As we can see Nmap absolutely spamms port 80 with requests and packets, then it pings the device to see if it is online.

<img width="2416" height="1248" alt="image" src="https://github.com/user-attachments/assets/8d2b0f5f-347b-4de9-992e-f067ca32ee9b" />

## F

to install ngrep you simply run ```$ sudo apt install ngrep```. if needed you can run ```$ sudo apt-get update``` first.

Below you can see the command for only seeing trafic containing nmap

<img width="1930" height="1262" alt="image" src="https://github.com/user-attachments/assets/514444ab-5f35-440d-9af6-7247e9a1a89b" />
