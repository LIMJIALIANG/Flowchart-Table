```mermaid
flowchart TB
BEGIN(["Start"])
STOP(["END"])

BEGIN --> B[/"Input templength, width"/]
B --> C["counter = 0"]

C --> D{"width > length"}

D1["length = width - (1.6*2) <br> width = templength - (1.6*2) </br>"]
D2["length = templength - (1.6*2) <br> width = width - (1.6*2) </br>"]

D --> |"TRUE"|D1

D --> |"FALSE"|D2

D1 & D2 --> E["length = round(length * 1000.00) / 1000.0 <br>
               width = round(width * 1000.00) / 1000.0 </br>"]
               
E --> F1{"length >= 3 && width >= 1"}

G11[/"Display 'We would suggest you to choose Rectangle Shade <br> with 12 seaters as the first choice.' </br>"/]
COUNT1["counter += 1"]

F1 --> |"TRUE"|G11 --> COUNT1
F1 --> |"FALSE"|F2

COUNT1 --> F2{"length >= 3 && width >= 1.3"}

H11{"counter == 0"}
H12{"counter == 1"}
G21[/"Display 'We would suggest you to choose Oval Stefan <br> with 10 seaters as the first choice.' </br>"/]
G22[/"Display 'We would suggest you to choose Oval Stefan <br> with 10 seaters as the second choice.' </br>"/]
COUNT2["counter += 1"]


F2 --> |"TRUE"|H11
H11 --> |"TRUE"|G21 --> COUNT2
H11 --> |"FALSE"|H12

H12 --> |"TRUE"|G22 --> COUNT2
H12 --> |"FALSE"|STOP

COUNT2 --> F3{"length >= 2.1 && width >= 1"}

H21{"counter == 0"}
H22{"counter == 1"}
G31[/"Display 'We would suggest you to choose Rectangle Bertha <br> with 8 seaters as the first choice.' </br>"/]
G32[/"Display 'We would suggest you to choose Rectangle Bertha <br> with 8 seaters as the second choice.' </br>"/]
COUNT3["counter += 1"]


F3 --> |"TRUE"|H21
H21 --> |"TRUE"|G31 --> COUNT3
H21 --> |"FALSE"|H22

H22 --> |"TRUE"|G32 --> COUNT3
H22 --> |"FALSE"|STOP

COUNT3 --> F4{"length >= 1.5 && width >= 1.5"}

H31{"counter == 0"}
H32{"counter == 1"}
G41[/"Display 'We would suggest you to choose Round Nadine <br> with 8 seaters as the first choice.' </br>"/]
G42[/"Display 'We would suggest you to choose Round Nadine <br> with 8 seaters as the second choice.' </br>"/]
COUNT4["counter += 1"]


F4 --> |"TRUE"|H31
H31 --> |"TRUE"|G41 --> COUNT4
H31 --> |"FALSE"|H32

H32 --> |"TRUE"|G42 --> COUNT4
H32 --> |"FALSE"|STOP

COUNT4 --> F5{"length >= 1.35 && width >= 1.35"}

H41{"counter == 0"}
H42{"counter == 1"}
G51[/"Display 'We would suggest you to choose Round Emma <br> with 6 seaters as the first choice.' </br>"/]
G52[/"Display 'We would suggest you to choose Round Emma <br> with 6 seaters as the second choice.' </br>"/]
COUNT5["counter += 1"]


F5 --> |"TRUE"|H41
H41 --> |"TRUE"|G51 --> COUNT5
H41 --> |"FALSE"|H42

H42 --> |"TRUE"|G52 --> COUNT5
H42 --> |"FALSE"|STOP

COUNT5 --> F6{"length >= 1.5 && width >= 0.9"}

H51{"counter == 0"}
H52{"counter == 1"}
G61[/"Display 'We would suggest you to choose Rectangle Niklas <br> with 6 seaters as the first choice.' </br>"/]
G62[/"Display 'We would suggest you to choose Rectangle Niklas <br> with 6 seaters as the second choice.' </br>"/]
COUNT6["counter += 1"]


F6 --> |"TRUE"|H51
H51 --> |"TRUE"|G61 --> COUNT6
H51 --> |"FALSE"|H52

H52 --> |"TRUE"|G62 --> COUNT6
H52 --> |"FALSE"|STOP

COUNT6 --> F7{"length >= 1.3 && width >= 0.8"}

H61{"counter == 0"}
H62{"counter == 1"}
G71[/"Display 'We would suggest you to choose Rectangle Heinrich <br> with 6 seaters as the first choice.' </br>"/]
G72[/"Display 'We would suggest you to choose Rectangle Heinrich <br> with 6 seaters as the second choice.' </br>"/]
COUNT7["counter += 1"]


F7 --> |"TRUE"|H61
H61 --> |"TRUE"|G71 --> COUNT7
H61 --> |"FALSE"|H62

H62 --> |"TRUE"|G72 --> COUNT7
H62 --> |"FALSE"|STOP

COUNT7 --> F8{"length >= 0.9 && width >= 0.9"}

H71{"counter == 0"}
H72{"counter == 1"}
G81[/"Display 'We would suggest you to choose Square Lea <br> with 4 seaters as the first choice.' </br>"/]
G82[/"Display 'We would suggest you to choose Square Lea <br> with 4 seaters as the second choice.' </br>"/]
COUNT8["counter += 1"]


F8 --> |"TRUE"|H71
H71 --> |"TRUE"|G81 --> COUNT8
H71 --> |"FALSE"|H72

H72 --> |"TRUE"|G82 --> COUNT8
H72 --> |"FALSE"|STOP

COUNT8 --> F9{"length >= 0.76 && width >= 0.76"}

H81{"counter == 0"}
H82{"counter == 1"}
G91[/"Display 'We would suggest you to choose Rectangle Heinrich <br> with 6 seaters as the first choice.' </br>"/]
G92[/"Display 'We would suggest you to choose Rectangle Heinrich <br> with 6 seaters as the second choice.' </br>"/]
COUNT9["counter += 1"]


F9 --> |"TRUE"|H81
H81 --> |"TRUE"|G91 --> COUNT9
H81 --> |"FALSE"|H82

H82 --> |"TRUE"|G92 --> COUNT9
H82 --> |"FALSE"|STOP
```
