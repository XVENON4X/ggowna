<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>ggowna</title>
    <meta name="generator" content="Jekyll v3.10.0" />
    <meta property="og:title" content="ggowna" />
    <meta property="og:locale" content="en_US" />
    <link rel="canonical" href="https://xvenon4x.github.io/ggowna/" />
    <meta property="og:url" content="https://xvenon4x.github.io/ggowna/" />
    <meta property="og:site_name" content="ggowna" />
    <meta property="og:type" content="website" />
    <meta name="twitter:card" content="summary" />
    <meta property="twitter:title" content="ggowna" />
  </head>
  <body>
    <div class="container-lg px-3 my-5 markdown-body">
      <h1>Witaj na stronie ggowna</h1>

      <p>Skopiuj poniższy kod i uruchom go w PowerShell na swoim komputerze:</p>
      
      <pre>
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
      </pre>

      <p>Jeśli masz już zainstalowanego Pythona, skrypt wykona się poprawnie i wypisze "Hello World!" na ekranie.</p>

    </div>
  </body>
</html>
