# sim756.TOTP
RFC 6238 (TOTP) - Time-Based One-Time Password Generator.

[https://www.nuget.org/packages/sim756.TOTP](https://www.nuget.org/packages/sim756.TOTP)

[https://github.com/sim756/sim756.TOTP](https://github.com/sim756/sim756.TOTP)

```c#
string totp = new TOTPGenerator().Compute("QWERTYUIOPASDFGH");
```
```c#
string nextTotp = new TOTPGenerator().Compute("QWERTYUIOPASDFGH", DateTime.UtcNow.AddSeconds(30));
```
```c#
string hotp = new TOTPGenerator()
{
  KeyString = "QWERTYUIOPASDFGH",
  Length = 6,
  Steps = 30
}.Compute();
```

> ## For HOTP, please check this library:
> NuGet - [sim756.HOTP](https://www.nuget.org/packages/sim756.HOTP) - https://www.nuget.org/packages/sim756.HOTP</br> 
> GitHub - [sim756.HOTP](https://www.github.com/sim756/sim756.HOTP) - https://www.github.com/sim756/sim756.HOTP
