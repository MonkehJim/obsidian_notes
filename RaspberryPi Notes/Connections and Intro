Above is a diagram of the RPi 4b GPIO Pinout (This will come to be useful when doing breadboard activities and **assigning pins relating to the project stuff**)

# 1. Connecting to the Pi (headlessly)
Previously, I figured out how to do this using PuTTY but it is now set up to go through VS Code, making it much easier to run.
Open VSCode and do `ctrl+shift+P` to open up the command dropdown.
`ssh carlinh@raspberrypi.local` will attempt to connect to the pi using my username that is registered on there. 
```
username: carlinh
password: 1234
```

As this was already previously set up, it should recover its memory when repeating **but if not...**

![[Pasted image 20240308230755.png]]

Open up the **File Explorer** and select 'open folder' then click OK. Default directory should be on `/home/carlinh`. This opens up all files available on the Pi and here we can find the dedicated Python Work file to save and run programs.

# 2. Editing and Running programs
Same as usual really but gets a bit tricky with running the program itself from your computer. Open the file you'd like to run, **make sure its saved to the Pi** then go to Run -> Run without debugger.

![[Pasted image 20240308231233.png]]

**If an error does occur**, check the terminal that opens at the bottom of the editor.

# 3. Keeping the script running after terminating connection (& running it through the terminal)
On the Pi is a command called `screen` which allows me to run the program as its own entity after the connection has been cut from the machine that initialised it. **Open a new terminal using the command dropdown `ctrl+shift+P`**. To screen a script (python specific), go to the directory of the file you want, find the file using dir (to see what's in the current directory) then run it as below:
``` Example
cd python\ work
screen python3 led\ test.py
```

This doubles as running the script using screen and also demonstrating how to execute any script through the command terminal. **All of this can be done through the SSH access in VS Code.**
![[Pasted image 20240308233227.png]]
![[Pasted image 20240308233306.png]]
# 4. Killing a script and a screen
To remove a screen we can **open up another terminal** and type `screen -ls`. This will list all screens currently active or inactive. To remove a screen we are going to do:
```
screen -S [SCREEN ID] -X quit
```

The screen ID is the first 4 ish numbers from the `screen -ls` command from earlier.
![[Pasted image 20240308233711.png]]
So to kill this screen, we do:
```
screen -S 3094 -X quit
```

![[Pasted image 20240308233820.png]]
**For scripts that are running while still connected, do `sudo killall python`**
