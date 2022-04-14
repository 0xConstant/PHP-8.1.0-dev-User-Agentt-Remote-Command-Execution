# ExploitDev Journey #11 | PHP 8.1.0-dev - 'User-Agentt' Remote Command Execution
Original Exploit: https://www.exploit-db.com/exploits/49933 <br>

**Exploit name:** PHP 8.1.0-dev - 'User-Agentt' RCE <br>
**CVE**: N\\A <br>
**Lab**: Knife - HackTheBox


### Description
There is a backdoor in PHP 8.1.0 developer version where you could execute system commands by using a specific HTTP header called `User-Agentt`.

<br>

### How it works
This exploit is very easy to understand and it doesn't require much work. A backdoor was introduced in PHP 8.1.0-dev that could allow attackers to execute system commands using a HTTP header that is very similar to `User-Agent` but it ends with double `t`. Your command goes inside a function called `zerodiumsystem(arg)` and then they are executed.

Manual RCE:
<img src="https://i.ibb.co/1q00d9V/knife1.png">

As you can see I have executed multiple commands by using a semicolon to separate them from one another and execute them one after the other.

<br>

### Writing the exploit
Writing the exploit is very similar to what you have already learned before, there is nothing new, except this time we split our HTML response content differently.

<br>

### Final thoughts
Unfortunately, there was nothing new in this session, you have learned a lot of new things so far but try to get a reverse shell on this machine by using a payload as a way to challenge yourself.


