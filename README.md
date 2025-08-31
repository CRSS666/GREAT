# GREAT

Welcome to the GREAT Redstone Enabled Automatic Transit (GREAT) system's documentation!

This repository includes information about how our systems work, and how expansions or
integration with other systems should be built.

If you're interested in contributing -- either to the docs or to the system itself -- 
contact [WorldWidePixel](https://WorldWidePixel.ca) or [Blurry](https://blurry.gay) on the [CRSS Discord](https://discord.crss.cc).

## Index

Things *may* get long, so for future-proofing we'll include a chapter index.

1. The System
    - Track Tile Grid

## 1. The System

GREAT is an easily-expansible and resource-efficient railway transit system.

### Track tile grid

The track tiles are based on a `9-1-9-1` grid (see the example below).

| Block          | Character |
|----------------|-----------|
| Cobblestone    | `c`       |
| Redstone Torch | `T`       |
| Torch          | `t`       |
| Rail           | `r`       |
| Powered Rail   | `R`       | 
| Air            | *empty*   |

```txt
                   === Base Layer ===

>  1     9     1     9     1     9     1     9      >
>  c ccccccccc c ccccccccc c ccccccccc c ccccccccc  >
>  c t       t c t       t c t       t c t       t  >
>  c ccccccccc c ccccccccc c ccccccccc c ccccccccc  >


                   === Rail Layer ===

>  1     9     1     9     1     9     1     9      >
>  R rrrrrrrrr R rrrrrrrrr R rrrrrrrrr R rrrrrrrrr  >
>  T           T           T           T            >
>  R rrrrrrrrr R rrrrrrrrr R rrrrrrrrr R rrrrrrrrr  >
```