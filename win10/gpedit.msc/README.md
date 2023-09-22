### 윈도우 10 홈에디션에 gpedit.msc 설치하기   
~~~
@echo off 
pushd “%~dp0” 
dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt 
dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt 
for /f %%i in (‘findstr /i . List.txt 2^>nul’) do dism /online /norestart /add-package:”%SystemRoot%\servicing\Packages\%%i” 
pause
~~~
~~~
C:\Users\~\Downloads>gpedit-enabler.bat

배포 이미지 서비스 및 관리 도구
버전: 10.0.18362.1379

이미지 버전: 10.0.18363.1556

1 중 1을(를) 처리하는 중 - Microsoft-Windows-GroupPolicy-ClientExtensions-Package~31bf3856ad364e35~amd64~en-US~10.0.18362.1 패키지를 추가하는 중
[==========================100.0%==========================]
작업을 완료했습니다.

배포 이미지 서비스 및 관리 도구
버전: 10.0.18362.1379

이미지 버전: 10.0.18363.1556

1 중 1을(를) 처리하는 중 - Microsoft-Windows-GroupPolicy-ClientExtensions-Package~31bf3856ad364e35~amd64~ko-KR~10.0.18362.1 패키지를 추가하는 중
[==========================100.0%==========================]
작업을 완료했습니다.

배포 이미지 서비스 및 관리 도구
버전: 10.0.18362.1379

이미지 버전: 10.0.18363.1556

1 중 1을(를) 처리하는 중 - Microsoft-Windows-GroupPolicy-ClientExtensions-Package~31bf3856ad364e35~amd64~~10.0.18362.1139 패키지를 추가하는 중
[==========================100.0%==========================]
작업을 완료했습니다.

배포 이미지 서비스 및 관리 도구
버전: 10.0.18362.1379

이미지 버전: 10.0.18363.1556

1 중 1을(를) 처리하는 중 - Microsoft-Windows-GroupPolicy-ClientTools-Package~31bf3856ad364e35~amd64~en-US~10.0.18362.1474 패키지를 추가하는 중
[==========================100.0%==========================]
작업을 완료했습니다.

배포 이미지 서비스 및 관리 도구
버전: 10.0.18362.1379

이미지 버전: 10.0.18363.1556

1 중 1을(를) 처리하는 중 - Microsoft-Windows-GroupPolicy-ClientTools-Package~31bf3856ad364e35~amd64~ko-KR~10.0.18362.1474 패키지를 추가하는 중
[==========================100.0%==========================]
작업을 완료했습니다.

배포 이미지 서비스 및 관리 도구
버전: 10.0.18362.1379

이미지 버전: 10.0.18363.1556

1 중 1을(를) 처리하는 중 - Microsoft-Windows-GroupPolicy-ClientTools-Package~31bf3856ad364e35~amd64~~10.0.18362.1474 패 키지를 추가하는 중
[==========================100.0%==========================]
작업을 완료했습니다.
계속하려면 아무 키나 누르십시오 . . .

C:\Users\~\Downloads>
~~~
