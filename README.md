if (-not (Get-Command python)) {
    # Pobierz i zainstaluj Pythona
    $installer = "$env:TEMP\python-installer.exe"
    Invoke-WebRequest -Uri "https://www.python.org/ftp/python/3.12.0/python-3.12.0-amd64.exe" -OutFile $installer
    Start-Process -FilePath $installer -ArgumentList "/quiet InstallAllUsers=1 PrependPath=1" -Wait
    Remove-Item $installer -Force
}

if (Get-Command python) {
    $script = "print('Hello World!')"
    $script | Set-Content -Path "$env:TEMP\test.py"
    python "$env:TEMP\test.py"
}
