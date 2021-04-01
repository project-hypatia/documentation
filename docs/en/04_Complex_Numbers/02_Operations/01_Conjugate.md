---
author: Michel Petit / Cogito Ergo Dev
date: 2021-04-01
---


 - `Hypatia\Number\Complex\Cartesian\Binary\compute_conjugate(float $r, float $i): array`
 - `Hypatia\Number\Complex\Polar\Binary\compute_conjugate(float $rho, float $phi): array`
 - `Hypatia\Number\Complex\Cartesian\Unary\conjugate(Cartesian $c): Cartesian`

# Using basic array type

```php

use Hypatia\Number\Complex\Cartesian\Binary as CBinary;
use Hypatia\Number\Complex\Polar\Binary as PBinary;


// Array as cartesian parts Re(z) and Im(z)
CBinary\compute_conjugate(1.0, 2.0); // [1.0, -2.0]

// Array as polar parts rho and phi
PBinary\compute_conjugate(1.0, pi()/2); // TODO

// Curried
$cconj = CBinary\compute_conjugate(1);
$cconj(2); // [1.0, -2.0]
$cconj(-6); // [1.0, 6.0]

$pconj = PBinary\compute_conjugate(1);
$pconj(pi()/4); // TODO
$pconj(-pi()); // TODO
```

# Using Cartesian class

```php
use Hypatia\Number\Complex\Cartesian;
use Hypatia\Number\Complex\Cartesian\Unary;

Unary\conjugate(new Cartesian(1, 2)); // Cartesian(1.0, -2.0)
```

# Using Polar class


```php
use Hypatia\Number\Complex\Polar;
use Hypatia\Number\Complex\Polar\Unary;

Unary\conjugate(new Polar(2, pi()/2)); // Polar(2, -pi()/2)
```