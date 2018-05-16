# Open Planetary Time Specification

- [Abstract](#abstract)
- [Units](#units)
- [Calculation](#calculation)
- [Planet References](#planet-references)

## Abstract

Open Planetary Time (OPT) is a time system that splits the day into 1,000 equals slices. OPT works on every planet, dwarf planet or minor planet that has a mean solar time.
It is independent from time zones and does not have a daylight saving time.
The basic unit is Spin (Sp). On earth one Spin is exactly 24 hours. Other time spans are described with unit prefixes of the metric system, e.g. Millispin (mSp). On earth one Millispin equals 1.44 minutes.
The OPT can describe time spans and concrete times. For example _mSp 500_ on earth equals 12:00 UTC. _"The process lasts 1 Spin"_ means it takes one day.

## Units

The main units are Spin (Sp) and Millispin (mSp). The symbol Sp does not conflict with the international system of units (s = Seconds, S = Siemens).

| Unit  | Symbol | Earth equivalent | Mars equivalent |
|:---|:---|:---|:---|
| Spin | Sp | 1 Day or 24 Hours | 1 Sol or 24.66 Hours |
| Millispin | mSp | 0.001 Day or 1.44 Minutes | 0.001 Sol or 1.48 Minutes |

All other combinations of the metric unit prefixes like Megaspin (MSp) or Microspin (μSp) are also possible. The units Decispin (dSp) and Centispin (cSp) are correct units but are not recommended to use.

## Calculation

Hours, Minutes and Seconds are in UTC.

`Sp = (Hours * 3600 + Minutes * 60 + Seconds) / 86400.0`
`mSp = (Hours * 3600 + Minutes * 60 + Seconds) / 86.4`

Example:

`18:30 UTC` ≙ `(18 * 3600 + 30 * 60) / 86.4` = `770.8`

## Planet References

If Spin is used without a reference planet the inhabited planet is being taken as reference. If a person lives on earth and mentions Spin, Earth-Spin is the correct time. The planet can be added to the symbol as suffix. The symbol for Earth-Millispin is mSpE, one Mars-Spin is 1 SpM.

| Planet  | Planet Acronym | Unit/Symbol for Spin | Unit/Symbol for Millispin |
|:---|:---|:---|:---|
| Mercury (Hermes) | H | SpH | mSpH |
| Venus | V | SpV | mSpV |
| Earth | E | SpE | mSpE |
| Mars | M | SpM | mSpM |
| Jupiter | J | SpJ | mSpJ |
| Saturn | S | SpS | mSpS |
| Uranus | U | SpU | mSpU |
| Neptune | N | SpN | mSpN |

For using OPT on other planets outside of our solar system the planet name can be added as suffix to the unit with [UpperCamelCasing](https://en.wikipedia.org/wiki/Camel_case). For Kepler-22b the units are SpKepler22B or mSpKepler22B, for COROT-7b it is SpCorot7B or mSpCorot7B.