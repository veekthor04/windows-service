# windows-service

This app creates a Python Windows Service

## Usage
- Install requirements

``pip install requirements.txt``

- Install the latest pywin32.exe 

Download and install pywin32 exe, for 32bit pywin32-302.win32-py3.x.exe, for 64 bit pywin32-302.win-amd64-py3.x.exe

``https://github.com/mhammond/pywin32/releases``

- Compile your server.py using pyinstaller

``pyinstaller --onefile server.py --hidden-import=win32timezone --clean --uac-admin``

- Install & Run service exe  (Run CMD as Administrator)

``cd dist``

``server.exe install``

``server.exe start``

``server.exe stop``

``server.exe remove``

``for /f "tokens=5" %a in ('netstat -aon ^| find ":5000" ^| find "LISTENING"') do taskkill /f /pid %a``