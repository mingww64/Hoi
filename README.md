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

Configure your `camera` options.
Copy files under /res to its correspended directory.

```shell
systemctl --user daemon-reload
systemctl --user enable microphone # [1]
systemctl daemon-reload
```

```shell
systemctl enable camera # [1][2]
systemctl start camera
```

**[1]** Always on and keep reconnecting when connection is dropped.  
**[2]** High battery cosumption.  

See also  

- [Roadmap of Hoi](https://felicia.pages.dev/2022/07/24/howdy的安装经历/)  
