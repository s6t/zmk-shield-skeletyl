# Skeletyl

ZMK shield config for flexiable PCB version of Skeletyl keyboard.

## Components ##
- https://github.com/Bastardkb/Skeletyl-PCB-plate
- https://github.com/Bastardkb/TBK-Mini-PCB-thumb-cluster
- https://github.com/Bastardkb/Elite-C-holder

## Usage

#### `config/west.yml`
``` yml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: s6t
      url-base: https://github.com/s6t
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-shield-skeletyl
      remote: s6t
      revision: main
  self:
    path: config
```

#### `build.yaml`
``` yml
include:
  - board: nice_nano_v2
    shield: skeletyl_left
  - board: nice_nano_v2
    shield: skeletyl_right
```
