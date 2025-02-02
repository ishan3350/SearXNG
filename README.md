
# Docker compose to deploy SearXNG

#### What's different than default docker compose?

Enabled the json support and disabled the rate limit for SearXNG API

#### How to use it?

git clone https://github.com/ishan3350/SearXNG

$randomBytes = New-Object byte[] 32
(New-Object Security.Cryptography.RNGCryptoServiceProvider).GetBytes($randomBytes)
$secretKey = -join ($randomBytes | ForEach-Object { "{0:x2}" -f $_ })
(Get-Content searxng/settings.yml) -replace 'ultrasecretkey', $secretKey | Set-Content searxng/settings.yml

##### docker-compose up -d



#### How to access it?

http://localhost:8080


