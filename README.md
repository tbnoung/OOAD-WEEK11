#ธีรศักดิ์ บัวไขย์ 57030175
# OOAD-WEEK11
State Diagram

1.
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
