# GREAT

Welcome to the GREAT Redstone Enabled Automatic Transit (GREAT) system's documentation!

This repository includes information about how our systems work, and how expansions or
integration with other systems should be built.

If you're interested in contributing -- either to the docs or to the system itself -- 
contact [WorldWidePixel](https://WorldWidePixel.ca) or [Blurry](https://blurry.gay) on the [CRSS Discord](https://discord.crss.cc).

## Index

Things *may* get long, so for future-proofing we'll include a chapter index.

1. [The System](./#1-the-system)
    - [Track Tile Grid](./#track-tile-grid)
        - [Station Stops](./#station-stops)

## 1. The System

GREAT is an easily-expansible and resource-efficient railway transit system.

### Track tile grid

The track tiles are based on a `9-1-9-1` grid (see the example below).

| Block           | Character   |
|-----------------|-------------|
| Cobblestone     | `c`         |
| Redstone Torch  | `T`         |
| Torch           | `t`         |
| Rail            | `r`         |
| Powered Rail    | `R`         | 
| Air             | *empty*     |
| Grid spacing    | `-`         |
| Direction signs | `<` and `>` |

```txt
=== Base Layer ===

>       9     1     9     1     9     1     9     1  >
>   ccccccccc-c-ccccccccc-c-ccccccccc-c-ccccccccc-c  >
>   t       t-c-t       t-c-t       t-c-t       t-c  >
>   ccccccccc-c-ccccccccc-c-ccccccccc-c-ccccccccc-c  >


=== Rail Layer ===

>       9     1     9     1     9     1     9     1  >
>  >rrrrrrrrr-R-rrrrrrrrr-R-rrrrrrrrr-R-rrrrrrrrr-R> >
>            -T-         -T-         -T-         -T  >
>  <rrrrrrrrr-R-rrrrrrrrr-R-rrrrrrrrr-R-rrrrrrrrr-R< >
```
#### Station Stops

Station stops are a little more complicated. We use angled Powered Rails
and buttons or redstone signals to make the minecarts stop and accelerate
in a convenient way for the passenger.

| Block       | Character | Front-view Character | Rail Type | Type Character |
|-------------|-----------|----------------------|-----------|----------------|
| Rail        | `r`       | `-`                  | Powered   | `+`            |
| Angled Rail | `R`       | `\` or `/`           | Normal    | `-`            |

```txt
=== Top-Down View - Station Stop ===

>              | > 
> >rrrRRrrrr>  | > --++-----
>              | > 
> <rrrrRRrrr<  | > -----++--
>              | > 


=== Side View - Station Stop ===

> >---  ---->  | > --+  ----
>     \/       | >    +-
>              | >
> <----  ---<  | > ----  +--
>      \/      | >     -+
```
