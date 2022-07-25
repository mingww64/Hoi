# Hoi
A set of configurations for [Howdy](https://github.com/boltgolt/howdy) face unlock with [IP Webcam](https://market.android.com/details?id=com.pas.webcam).  

Environment:

```zsh
❯ neofetch
██████████████████  ████████   project@hoi 
██████████████████  ████████   --------------- 
██████████████████  ████████   OS: Manjaro Linux x86_64 
██████████████████  ████████   Kernel: 5.19.0-1-MANJARO 
████████            ████████   DE: Plasma 5.24.6 
████████  ████████  ████████   WM: KWin
████████  ████████  ████████
████████  ████████  ████████
████████  ████████  ████████
████████  ████████  ████████
████████  ████████  ████████
████████  ████████  ████████
████████  ████████  ████████
████████  ████████  ████████
                               

                            Project Hoi. 
                            Copyright (C) 2022 Felicia Wen

~/Project/Hoi/res ❯ 
```

## Installation

### Manual

#### Howdy integration  

Configure your `camera` options in files under res/ .
Copy Configured files to its correspended directory.
Now howdy is integrated with IP Webcam.  

#### Recording

```shell
systemctl --user daemon-reload
systemctl --user enable microphone # [1]
systemctl daemon-reload
```

Now the Microphone of IP Webcam will be sinked to PulseAudio once user login.

#### Camera

To run camera permanently.

`$ systemctl enable camera` *[1] [2] [3]*

rather than that,  
I suggest  
`$ systemctl start camera`  
do streaming stuff...  
`$ systemctl stop camera`  

----

**[1]** Always on and keep reconnecting when connection is dropped.  
**[2]** High battery cosumption.  
**[3]** You need to resume it after suspended or hibernated, manually or by adding an [systemd service](res/.config/systemd/user/afterhibernate.service).

See also  

- [Roadmap of Hoi](https://felicia.pages.dev/2022/07/24/howdy的安装经历/)  
