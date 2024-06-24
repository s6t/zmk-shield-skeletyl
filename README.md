# Skeletyl

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
      path: config/boards/shields/skeletyl
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