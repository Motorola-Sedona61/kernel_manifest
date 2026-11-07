# Motorola SM6375 kernel manifest

Pinned kernel and module sources for Fogos and Rhodep, based on Motorola `MMI-W1UOS36H.35-39-7` (Linux 6.1.145). Kernel, display and graphics retain Motorola history. Fogos and Rhodep module sources share `motorola-kernel-modules`, branch `sedona-6.1`; retained Fogos drivers are under `legacy/fogos`.

```sh
mkdir sedona-kernel
cd sedona-kernel
repo init -u https://github.com/Motorola-Sedona61/kernel_manifest.git -b main
repo sync -c -j8
./build/setup.sh
./build.sh FOGOS
```

For Rhodep, run `./build.sh RHODEP`. Outputs are placed under `prebuilt/FOGOS/6.1` or `prebuilt/RHODEP/6.1`. The manifest links the tested build entrypoint at the workspace root.

[Host setup and Android build guide](https://github.com/Motorola-Sedona61/guide).
