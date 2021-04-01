---
author: Michel Petit / Cogito Ergo Dev
date: 2021-04-01
---


This is only available for Cartesian form. Useless in Polar form as it is in definition.

 - `Hypatia\Number\Complex\Cartesian\Binary\compute_modulus(float $r, float $i): float`
 - `Hypatia\Number\Complex\Cartesian::modulus(): float`

# Using float

Simple function example, both full call and curried call:

```php
use Hypatia\Number\Complex\Cartesian\Binary;

Binary\compute_modulus(3.0, -4.0); // 5.0

// curried
$mod = Binary\compute_modulus(3.0);
$mod(4.0); // 5.0
$mod(-4.0); // 5.0
```

# Using Cartesian class

Using object of class Cartesian calling method `Cartesian::modulus()`:

```php
use Hypatia\Number\Complex\Cartesian;

$z = new Cartesian(3.0, -4.0);
$z->modulus(); // 5.0
```

As modulus is a property of complex number, it is ok to have a method in the
object to get its value.
