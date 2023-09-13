
- Copy file iwpriv /data/local/tmp
- Open Terminal Android root
- chmod +x /data/local/tmp/iwpriv
- Open NetHunter App
- Pilih Custom Commands
- Edit Start wlan0 monitor mode
  Command :
  `echo -ne "\033]0;Wlan0 Monitor Mode\007"&& clear;su -c "echo 4 > /sys/module/wlan/parameters/con_mode;ip link set wlan0 down;ip link set wlan0 up;/data/local/tmp/iwpriv wlan0 monitor 1;/data/local/tmp/iwpriv wlan0 MonitorModeConf 1 40 1 111 0";sleep 2 && exit `

  Ket : 1  = Chanel (1-13)
        40 = Bandwidth (20/40)

- Run > Start wlan0 monitor mode
   
- Add Custom Command
  Label :
  Launch Wifite wlan0
  Command :
  ` echo -ne "\033]0;Wifite wlan0\007" && clear;wifite -i wlan0 `
  Send to : kali
  Exec mode : interactive
  
- Run > Launch Wifite wlan0
