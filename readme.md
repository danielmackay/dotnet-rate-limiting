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

The script sends 1 request per second.  The rate limiter allows 4 requests per 12 seconds.  As the test runs for 24 seconds we see 8 sucessful requests and 16 failed requests.  This gives 33% success and 66% failure as shown by K6:

<img width="1352" alt="image" src="https://user-images.githubusercontent.com/2636640/200818015-3ad0007b-836e-4b38-a05d-6b4d8007f589.png">

## Resources
[Microsoft Docs | Rate Limiting](https://learn.microsoft.com/en-us/aspnet/core/performance/rate-limit?view=aspnetcore-7.0)
