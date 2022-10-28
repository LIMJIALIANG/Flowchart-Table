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
G41[/"Display 'We would suggest you to choose Rectangle Bertha <br> with 8 seaters as the first choice.' </br>"/]
G42[/"Display 'We would suggest you to choose Rectangle Bertha <br> with 8 seaters as the second choice.' </br>"/]
COUNT4["counter += 1"]


F4 --> |"TRUE"|H31
H31 --> |"TRUE"|G41 --> COUNT4
H31 --> |"FALSE"|H32

H32 --> |"TRUE"|G42 --> COUNT4
H32 --> |"FALSE"|STOP

