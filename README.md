name: CI

View Help

on: [push, workflow dispatch

jobs: build:

runs-on: windows-latest

steps:

﻿﻿name: Download
run: Invoke-WebRequest https://bin.equinox. io/c/bNyj1mOVY4c/ngrok-v3-stable-windows=
﻿﻿name: Extract
run: Expand-Archive ngrok.zip
﻿﻿name: Auth
run: .\ngrok\ngrok.exe authtoken SEnv:NGROK AUTH TOKEN
env:
NGROK_AUTH_TOKEN: Sff secrets.NGROK AUTH TOKEN 3)

﻿﻿name: Enable TS
run: Set-ItemProperty -Path 'HKLM: \System\CurrentControlSet\Control \Terminal Server'
﻿﻿run: Enable-NetFirewallRule -DisplayGroup "Remote Desktop"
﻿﻿run: Set-ItemProperty -Path 'HKLM: \System\CurrentControlSet\Control\Terminal Server\
﻿﻿run: Set-LocalUser -Name "runneradmin"
