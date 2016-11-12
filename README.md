#ธีรศักดิ์ บัวไขย์ 57030175
# OOAD-WEEK11
State Diagram

#1.
![](http://www.plantuml.com/plantuml/img/YzQALT1DqRLJSCqhIIqAoCpZWZ4Kh1JyynHIyqgAAe5CiAW2chnBle9ZSabcFeWTbfYJcP9OagfGWAn65sQoOsv-QLu95n8RRZxGN9ZvM5KXs-ASaPgShP08aR9HI4hCISnBJaNH0FPDU6P9HafHOdboOd465p87pRpG0h2ROUQWg0IwFLeh5W00)
##Code
[*] -d-> EnterPin

EnterPin : On entry : Enter Pin

EnterPin : Do Action : Validate pin

EnterPin --> EnterAmount

EnterAmount : On enter : Enter Amount

EnterAmount : Do Action : Check amount < balance

EnterAmount -d-> Withdrawcash

Withdrawcash : Do Action : Update balance

Withdrawcash -->[*]
#2.
![](http://www.plantuml.com/plantuml/img/VO-nRiCm34HtVyN1Om33kuSidRAq0Jm66HI9hWN8aa5I2VptjMK7A3fquC3ZkoDvEztHS7F6rp1KQw43HUMbTLxcO9P3gp-JcgVnmJm2rKKiBky2TP2NLpj2CqToI14jPk8XyGHHmvhdQWFHx7lMl3UwDh_OCQjBhxZ3VmyvnFeQo0Z1Ho5MMCEkFjBvZ9vuyV7x8ukcYVWIRSYEUXBnANORZ4inacijar62xCFgNsivlJnxuB1fcWFfzWH37ccBHFK3)
##Code
[*] -r-> Off

Off : entry/display

Off : "Notavailable"

Off -r-> idle: switch turned on / perform startup

idle --> Off : turned off / perform shutdown

idle : entry/display

idle : "Please insert card"

idle -r> SeryingCustomerIncludeSession:card Inserted/create session

SeryingCustomerIncludeSession --> idle:session completed or sborted 


#3.
![](http://www.plantuml.com/plantuml/img/YzQALT3LjLC8JYqfBU02amfM2Ydv-fbvcIMPYJcPLQaAnQcvcNc9HL1PtIAWSiUonCoSnAISL2uu2wSsX0hT5A1MjzAS72uG0T6G1bI3eXmi1LOPhHMBhjavCIyvDISr1UOM534O0s9mKMfQQLwAGa5YPMvgNaanGXPcDW00)
##Code
[*] --> Setup

Setup : do/initialize seminar

Setup -r-> Available

Available : do/initialize seminar

Available -d-> Full

Full : do/finalize seminar

Full -d-> [*]

Available -d-> Canceled

Setup -d-> Canceled

Canceled : do/refund payments

Canceled -d-> [*]

#4.
![](http://www.plantuml.com/plantuml/img/TP0n2yCW48LtVyND1N7lqA6GeL38r2baa6Yen9xbOY3vzqcZKLle9FUzztodpQa5Jlm2TzSDMh5mm1aqUbh4PypiBSTHI2lfTR0z-a1xE3fda1Lpk2K0zkC30VufSO35JLdZDYqJ6mjDRTgLtA1nqvh0ePV6QjN6beh8KLhlE_3N7YsyhExDlFr72eUNr9El-vgKfgnKi_7YXZjT0G00)
##Code
[*] -r-> Locked

Locked : entry/Lock

Locked : pass/alarm

Locked -r-> Unlocked : coin

Unlocked : entry/Unlock

Unlocked : coin / thank you

Unlocked -l-> Locked : pass

Unlocked -d-> Broken : [Unlock failed]/UnlockError

Locked -d-> Broken : [lock failed]/UnlockError

Broken --> Locked : fixed

Broken : entry/OutOfOrder

Broken : Exit/InOrder

