---
id: cviw3y1HnDNvr5Yxhz7dF
title: Lab2
desc: ''
updated: 1630950157709
created: 1630650940304
---

## [Question Set](https://drive.google.com/file/d/

1TxIzxSoEqgJITviQ6wIw20PAkE-eENga/view?usp=sharing)
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
[Video](/assets/Lab1_Q2_Parth_Shah_AU1940065.mp4)

### Question 3

```c
void main(){
   DDRA=0x55;
   while(1){
      PORTA=PINA>>1;
   }
}

```
[Video](/assets/Lab1_Q3_Parth_Shah_AU1940065.mp4)
<figure class="video_container">
  <video controls="true" allowfullscreen="true" >
    <source src="assets\Lab1_Q3_Parth_Shah_AU1940065.mp4" type="video/mp4">
  </video>
</figure>

![](/assets/images/Lab1_Q3_Circuit.jpeg)

