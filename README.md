# Line Follower
This was a project that has been done in the span of a day during a mini hackathon.
### Technical Tasks
The main objectives of this project were the following:
* assembly of the line follower in one of the course's labs;
* implementing basic algorithms to test the functionality of the components(DC motors running smoothly, the QTR-8A sensor giving proper feedback, etc.)
* to program a line follower with auto callibration for the sensors upon boot up;
* to implement and fine tune a PID controller which would enable the line follower to complete a test course as fast as possible(desired target was ~20 seconds).
### Components
* 1 Arduino Uno;
* 1 car chassis; 
* 1 ball caster; 
* 2 DC motors; 
* L293D motor driver;
* 2 wheels; 
* 1 QTR-8A reflectance sensor array; 
* wires (per logic).

---

## **Pictures of the setup.**

| ![pic1](./Syntax%20and%20setup/Back%20View.jpg) | ![pic2](./Syntax%20and%20setup/Front%20Angled%20View.jpg) | 
|:-------------:|:-------------:|
| ![pic3](./Syntax%20and%20setup/Side%20View.jpg) | ![pic4](./Syntax%20and%20setup/Top%20View.jpg) |

---

## **Picture of the team. (#Liniutzarii)**
![pic5](./team.jpeg)

---

## **Project challenges**
#### Auto Callibration
* In order to receive a higher score on our line follower, one of the main tasks was making it automatically calibrate the QTR-8A sensor. This was something much easier said than done, as the initial idea of giving the wheel motors timed intervals in which they would change direction proved to be ineffective. Due to hardware factors(one DC motor output more power than the other), the line follower couldn't remain centered on the black line, making a little pirouette during the automatic callibration.  
* After receiving tips and tricks from the course and lab teachers, we decided to opt for using the sensors as they were being callibrated. Starting from a centered position on the black line, the follower would turn left and once the rightmost sensor would be dead on the black line, the DC motors changed their direction of rotation. Then, once the leftmost sensor would be centered on the black line, the direction of rotation would be changed again, rinse and repeat.

### Video
Live course trial [here](https://youtu.be/STF4KL0HLZI).
