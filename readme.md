# .NET 7 Rate Limiter

## Setup

Install .NET 7

`winget install Microsoft.DotNet.SDK.6`

Install K6

`winget install k6`

## Run

```ps1
cd src
dotnet run
```

## Test

```ps1
cd test
k6 run .\script.js
```
