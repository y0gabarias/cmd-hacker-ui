@echo off
color 0a
title Hacker Tool - y0gabarias
mode con: cols=80 lines=25

:menu
cls
echo.
echo [ HACKING TERMINAL - y0gabarias ]
echo ---------------------------------
echo 1. Start DDoS Target [FAKE]
echo 2. Track IP Address
echo 3. Access CCTV [DEMO]
echo 4. Exit
echo ---------------------------------
set /p input=Select option: 

if "%input%"=="1" goto ddos
if "%input%"=="2" goto track
if "%input%"=="3" goto cctv
if "%input%"=="4" exit

:ddos
cls
echo Initializing DDoS to target: 192.168.0.1
echo Bypassing firewall...
ping -t 127.0.0.1 >nul
goto menu

:track
cls
set /p ip=Enter IP to trace: 
echo Scanning IP: %ip% ...
ping %ip% -n 2 >nul
echo Status: ONLINE
echo Location: Classified
echo ISP: ShadowLink Internet
echo Port 22: Open
pause
goto menu

:cctv
cls
echo Searching unsecured CCTV nodes...
echo Found: cam001.localnet
echo Accessing video stream...
echo [*] Feed available: StreetCam_42
pause
goto menu
