# Colemator Layout ZMK Module

This repository contains files for the layout I use on all my keyboards. 
To use it in your keymaps, add the module to the west.yml found in your zmk-config's config directory. 
There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the Colemator Layout module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: proostas
      url-base: https://github.com/proostas
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: colemator-layout-zmk-module
      remote: proostas
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it were in your config directory.
