# Qubic AMD GPU trainer

This is [Qubic](https://www.qubic.org) AMD GPU trainer (mining software), only support Windows (10 or 11), for Qubic Epoch 137 (2024.11.27 to 2024.12.4).

## You need to install

+ .NET 8.0 Runtime:
<https://aka.ms/dotnet-core-applaunch?missing_runtime=true&arch=x64&rid=win-x64&os=win10&apphost_version=8.0.10>
+ Microsoft Visual C++ Redistributable:
<https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170>
<https://aka.ms/vs/17/release/vc_redist.x64.exe>
+ AMD card driver:
<https://drivers.amd.com/drivers/whql-amd-software-adrenalin-edition-24.10.1-win10-win11-oct-rdna.exe>

## Supported cards

### Tested

+ gfx1010: RDNA  (AMD Radeon RX 5700)
+ gfx1011: RDNA  (AMD Radeon Pro 5600M)
+ gfx1031: RDNA2 (AMD Radeon RX 6700, 6700 XT, 6700M, 6750 XT, 6800M)
+ gfx1034: RDNA2 (AMD Radeon RX 6400, 6500 XT)

### Untested

+ gfx1030: RDNA2 (AMD Radeon RX 6800, 6800 XT, 6900 XT)
+ gfx1032: RDNA2 (AMD Radeon RX 6600, 6600 XT, 6650M, 6800s)
+ gfx1035: RDNA2 (AMD Radeon(TM) Graphics)
+ gfx1100: RDNA3 (AMD Radeon RX 7900 XT)
+ gfx1101: RDNA3 (AMD Radeon RX 7700 XT, 7800 XT)
+ gfx1102: RDNA3 (AMD Radeon RX 7600, 7600 XT)

## Performance for Qubic Epoch 137

+ For AMD Radeon RX 6700 XT, at GPU clock 2000 M and memory clock 2000 M, GPU Voltage 0.875 V: **550 it/s**, 120 W.
+ For AMD Radeon RX 6500 XT, at GPU clock 2000 M: 160 it/s.
+ For AMD Radeon RX 5700, at GPU clock 1700 M and memory clock 1750 M, GPU Voltage 0.9 V: 290 it/s, 120 W.

## Miner fee rate

### 16%

## Usage

+ Sign up <https://pool.qubic.li/>.
+ At "Settings", fill your Qubic Id (address), generate your "Access Token".
+ Edit `Qubic-AMD\appsettings.json`, change the "accessToken" to your own.
+ Run `Qubic-AMD\qli-Client.exe`.

### Skill

Run `qli-worker-gpu-amd-E137.exe AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA 0000000000000000000000000000000000000000000000000000000000000000 0 12` to test whether the algorithm kernel for AMD GPU can work properly.
