# thread-safe-counter
Made it at Ubuntu 18.04 and it works at Ubuntu 18.04 and WSL.

#Run with Mutex
![image](https://user-images.githubusercontent.com/68852298/121776546-79113280-cbc8-11eb-960f-9fd3fdf8805e.png)

#Run with Semaphore
![image](https://user-images.githubusercontent.com/68852298/121794830-6f2e1480-cc46-11eb-80ea-da5d0d0ac370.png)

#Performance
Using Semaphore takes much more time than using Mutex. Almost 30 times longer.

#Reason
Mutex uses very simple code and it can only determine two state lock or unlock. 
But Semaphore is more complex and it has more variables so it can determince more state.
