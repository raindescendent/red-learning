-Checking Processes (ps)-

-----------------------------------
[Command] 
> ps
[Output]
> Invoked Processes by the user

>> PID  TTY          TIME CMD
>> 9355 pts/1    00:00:00 bash
>> 9388 pts/1    00:00:00 ps
-----------------------------------

> PID: unique process ID assigned by kernel.

-----------------------------------
[Command] 
> ps aux
[Output]
> Invoked All the Processes by all users

>> USER        PID   %CPU %MEM   VSZ   RRS TTY      STAT START   TIME COMMAND
>> root        9280  0.0  0.0      0     0 ?        I<   14:59   0:00 [kworker/u17:
>> santigi+    9355  0.0  0.0 224572  5248 pts/1    Ss   15:02   0:00 bash
>> root        9424  0.0  0.0  16344  6400 ?        S    15:03   0:00 systemd-userw
>> root        9425  0.0  0.0  16344  6528 ?        S    15:03   0:00 systemd-userw
>> root        9426  0.0  0.0  16344  6400 ?        S    15:03   0:00 systemd-userw
>> root        9492  0.0  0.0      0     0 ?        I<   15:04   0:00 [kworker/u17:
>> santigi+    9532  0.0  0.0 226312  4864 pts/1    R+   15:06   0:00 ps aux

-----------------------------------

-Filtering Processes by name (ps)-

> ps aux | grep {processName}

[Command] 
> ps aux | grep {gnome}
[Output]
> Invoked All 'gnome' process/command name

>> USER        PID   %CPU %MEM VSZ    RRS   TTY     STAT START   TIME COMMAND
>> santigi+    1940  0.0  0.2 3168180 29108  ?      Ssl  12:02   0:00 /usr/bin/gjs -m /usr/share/gnome-shell/org.gnome.Shell.Notifications
>> santigi+    2047  0.1  4.4 1779192 527124 ?      Sl   12:02   0:19 /usr/bin/gnome-software --gapplication-service
>> santigi+    2172  0.0  0.2 3028896 28840  ?      Ssl  12:02   0:00 /usr/bin/gjs -m /usr/share/gnome-shell/org.gnome.ScreenSaver
>> santigi+    2545  0.0  1.0 2078044 122940 ?      Ssl  12:02   0:00 /usr/libexec/xdg-desktop-portal-gnome


-Filtering Processes by name (top)-

[Command]
> top
[Output]
> Dynamical Process Monitor


----------------------------------------------------------------------


-Managing Processes (niceness)-

> niceness: Used term to refeer the 'generosity' using the machine resources leaving a considerable amount of this for other processes. Decreasing or Increasing the process priority to the kernel.

> You are 'more nice' when you decrease the process priority and 'less nice' when you do the opposal.

>> Range of values (niceness): -20 to +19 // -20 lower values equals to more priority // 19 higher values equals to less priority.
>> 0 = default nice value.
>> At the process start the nice value (priority) is inherited from their parent process.
>> Owner: Can increase the nice value but cannot decrease. 
>> Root: Can arbitrary set of the process niceness.

-----------------------------------

-Setting Priority on Process Start (nice)-

> nice {nicenessValue} {processRelativePath} 
 
[Commands] 
> nice -n -10 /bin/slowprocess (More priority)
> nice -n 10 /bin/fastprocess (Less Priority)
[Output]
>> Open the process with more/less priority 
>> Change in 'ps aux' => stat value

-----------------------------------

-Changing Priority on Running Process (renice)- 

> renice {nicenessValue} {PID} 

[Command]
> renice -5 12038 
[Output]
>>12038 (process ID) old priority 0, new priority -5

-----------------------------------

-Renice with top command- 

[Command]
> top > 'r' key
[Outputs]
>> Process dynamical monitor
>> "r" => 'PID to renice: {PID}'
>> 'Renice PID {number} to value: {niceness}' 


----------------------------------------------------------------------


-Killing Processes-
> Problematic Process == 'rogue process'


> kill {signal} {PID}
> killall {signal} {name}

[Command]
> kill 15 12038 {killDefaultSignal} {calcPID}

>> Researchment of Signals required


----------------------------------------------------------------------


-Run Processes in Background / Foreground-

> Background: The program can execute and have a continuous running with any dependant of the terminal. 
> Using the '&' {Ampensand Symbol} at the end of the command. Sends the output as background process.  
OR
> bg {PID}

[Command]
> gnome-calculator &
[Output]
>> Runs the Calculator with the terminal open yet for receive new commands. 

-----------------------------------

> Foreground 
> fg {PID}

[Command]
> fg 12038 // {calcPID}


----------------------------------------------------------------------


-Scheduling Process- 

> Setting automatic task of a process

> crond // Suitable for every day, week, month
> at // Sets a daemon, called 'atd' useful for a future one-task purposes
> Many timeFormat preference: '7:20pm 05/21/2024' 

> at {hour} {date}

[Command]
> at 7:20pm 05/21/2024
[Output]
> Task to Run at defined time.
