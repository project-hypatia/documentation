---
title: From Complex to another Complex
author: Michel Petit / Cogito Ergo Dev
date: 2021-03-31
---



See now how to transform Complex Number to another Complex Number using some complex features.

# Conjugate

 - `Hypatia\Number\Complex\Cartesian\Binary\compute_conjugate(float $r, float $i): array`
 - `Hypatia\Number\Complex\Polar\Binary\compute_conjugate(float $rho, float $phi): array`
 - `Hypatia\Number\Complex\Cartesian\Unary\conjugate(Cartesian $c): Cartesian`


```php
use Hypatia\Number\Complex\Cartesian; // Class
use Hypatia\Number\Complex\Cartesian\Binary as CBinary;
use Hypatia\Number\Complex\Polar\Binary as PBinary;
use Hypatia\Number\Complex\Cartesian\Unary;

CBinary\compute_conjugate(1.0, 2.0); // [1.0, -2.0]
PBinary\compute_conjugate(1.0, pi()/2); // TODO

// Curried
$cconj = CBinary\compute_conjugate(1);
$cconj(2); // [1.0, -2.0]
$cconj(-6); // [1.0, 6.0]

$pconj = PBinary\compute_conjugate(1);
$pconj(pi()/4); // TODO
$pconj(-pi()); // TODO

Unary\conjugate(new Cartesian(1, 2)); // Cartesian(1.0, -2.0)
```

# Modulus

This is only available for Cartesian form. Useless in Polar form as it is in definition.

`Hypatia\Number\Complex\Cartesian\Binary\compute_modulus(float $r, float $i): float`

```php
use Hypatia\Number\Complex\Cartesian\Binary;

Binary\compute_modulus(3.0, -4.0); // 5.0

// curried
$mod = Binary\compute_modulus(3.0);
$mod(4.0); // 5.0
$mod(-4.0); // 5.0
```

# Argument

Again, this is only available for Cartesian form. Useless in Polar form as it is in definition.

`Hypatia\Number\Complex\Cartesian\Binary\compute_modulus(float $r, float $i): float`

```php
use Hypatia\Number\Complex\Cartesian\Binary;

Binary\compute_argument(-3, 3); // 3⋅pi/4

// curried
$arg = Binary\compute_argument(-3);
$arg(3); // 3⋅pi/4
```
