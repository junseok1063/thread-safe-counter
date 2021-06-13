# thread-safe-counter
Made it at Ubuntu 18.04 and it works at Ubuntu 18.04 and WSL.

#Run with Mutex
![image](https://user-images.githubusercontent.com/68852298/121776546-79113280-cbc8-11eb-960f-9fd3fdf8805e.png)

#Run with Semaphore
![image](https://user-images.githubusercontent.com/68852298/121794830-6f2e1480-cc46-11eb-80ea-da5d0d0ac370.png)
it 
#Performance
Using Semaphore takes much more time than using Mutex. Almost 30 times longer.

#Reason
Mutex uses very simple code and it can only determine two state lock or unlock. 
Also it can only be unlocked by something that lock itself. So while Running, it doesn`t need to consider
other exter factors.
But Semaphore is more complex and it has more variables so it can determine more state include lock and unlock. And many other variables
can unlock it so it need to be consider many other factor. So using Semaphore will cost more time.
