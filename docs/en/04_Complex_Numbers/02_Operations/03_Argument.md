---
author: Michel Petit / Cogito Ergo Dev
date: 2021-04-01
---



Again, this is only available for Cartesian form. Useless in Polar form as it is in definition.

 - `Hypatia\Number\Complex\Cartesian\Binary\compute_modulus(float $r, float $i): float`
 - `Hypatia\Number\Complex\Cartesian::argument(): float`

# Using float

Simple function example, both full call and curried call:

```php
use Hypatia\Number\Complex\Cartesian\Binary;

Binary\compute_argument(-3, 3); // 3⋅pi/4

// curried
$arg = Binary\compute_argument(-3);
$arg(3); // 3⋅pi/4
```

# Using Cartesian class

Using object of class Cartesian calling method `Cartesian::argument()`:

```php
use Hypatia\Number\Complex\Cartesian;

$z = new Cartesian(-3.0, 3.0);
$z->argument(); // 3⋅pi/4
```

As argument is a property of complex number, it is ok to have a method in the
object to get its value.
