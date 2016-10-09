Bia.Countries
=============

ISO-3166-1 country codes for .NET, forked from [ilyabreev's Bia.Countries].

ActiveDirectoryCompatibility branch of the project renames ISO-3166-1 country names to match names in Active Directory (Windows Server 2012 R2).

For example, while Active Directory has "United Kingdom", ISO-3166-1 specifies the name as "United Kingdom of Great Britain and Northern Ireland". Another example is that while Active Directory has "Russia", ISO-3166-1 specifies the name as "Russian Federation". But there are great many other countries that have similar discrepancies.

I have also added back all countries that no longer exist in the current ISO-3166-1 specification. I kept "Western Sahara" included in the library even though Active Directory does not recognize it.

C# example
-------------
```C#
var countries = new Iso3166Countries();
var valid = countries.IsNameValid("Russia"); // true
var alpha2 = countries.GetAlpha2CodeByName("Russia"); // RU
var numeric = countries.GetNumericCodeByName("Russia"); // 643
```

PowerShell example
-------------
```PowerShell
Import-Module "C:\Path\To\Bia.Countries.dll"
$countries = New-Object Bia.Countries.Iso3166Countries
$valid = $countries.IsNameValid("Russia") # true
$alpha2 = $countries.GetAlpha2CodeByName("Russia") # RU
$numeric = $countries.GetNumericCodeByName("Russia") # 643
```

Install
-------------


Resources
-------------
[Wikipedia](https://en.wikipedia.org/wiki/ISO_3166-1)

[ilyabreev's Bia.Countries]:https://github.com/ilyabreev/Bia.Countries
