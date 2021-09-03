---
id: 0vsXoFu0T3hAK2pzle2TP
title: Lab2
desc: ""
updated: 1630688841254
created: 1630650940304
---
## [Question Set](https://drive.google.com/file/d/1TxIzxSoEqgJITviQ6wIw20PAkE-eENga/view?usp=sharing)
### Question 2

```c
void main() {
     int i;
       DDRC=0x0f;
       while(1){
          PORTC=0x0f;
          for(i=0;i<42150;i++){
          }
          PORTC=0x00;
          for(i=0;i<42150;i++){
          }
       }
}
```
[Video](/assets/Q2_Parth_Shah_AU1940065.mp4)
<figure class="video_container">
  <iframe src="/assets/Q2_Parth_Shah_AU1940065.mp4" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
### Question 3

```c
void main(){
   DDRA=0x55;
   while(1){
      PORTA=PINA>>1;
   }
}

```
