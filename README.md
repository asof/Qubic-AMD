# Qubic AMD GPU trainer

This is [Qubic](https://www.qubic.org) AMD GPU trainer (mining software), only support Windows (10 or 11), for Qubic Epoch 141 (2024.12.25 to 2025.1.1).

## You need to install

+ [.NET 8.0 Runtime](https://aka.ms/dotnet-core-applaunch?missing_runtime=true&arch=x64&rid=win-x64&os=win10&apphost_version=8.0.10)
+ [Microsoft Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)
+ [AMD Radeon Graphics Driver](https://www.amd.com/en/support/download/drivers.html)

## Supported cards

### Tested

+ gfx1010: RDNA  (AMD Radeon RX 5700)
+ gfx1011: RDNA  (AMD Radeon Pro 5600M)
+ gfx1031: RDNA2 (AMD Radeon RX 6700, 6700 XT, 6700M, 6750 XT, 6800M)
+ gfx1034: RDNA2 (AMD Radeon RX 6400, 6500 XT)
+ gfx1102: RDNA3 (AMD Radeon RX 7600, 7600 XT)

### Untested

+ gfx1030: RDNA2 (AMD Radeon RX 6800, 6800 XT, 6900 XT)
+ gfx1032: RDNA2 (AMD Radeon RX 6600, 6600 XT, 6650M, 6800s)
+ gfx1035: RDNA2 (AMD Radeon(TM) Graphics)
+ gfx1100: RDNA3 (AMD Radeon RX 7900 XT)
+ gfx1101: RDNA3 (AMD Radeon RX 7700 XT, 7800 XT)

## Performance for Qubic Epoch 141

| AMD Radeon | Core clock | Voltage | it/s | qli it/s | Shares/12 hours | Solution/12 hours | Power |
|------------|------------|---------|------|----------|-----------------|-------------------|-------|
| RX 5700    | 1700 MHz   | 0.95 V  | 911  | 6377     | 7.08            | 0.0345            | 130 W |
| RX 6700 XT | 2000 MHz   | 0.875 V | 1090 | 7630     | 8.67            | 0.0422            | 110 W |
| RX 7600    | 2200 MHz   | 0.80 V  | 938  | 6566     | 7.61            | 0.037             | 90 W  |

Please use the numbers in "qli it/s" units to compare with the numbers listed at [pool.qubic.li](https://pool.qubic.li/en-US/hashrates).

The performance is poor and waiting optimization.

## Miner fee rate

### 9%

## Usage

+ Sign up <https://pool.qubic.li/>.
+ At "Settings", fill your Qubic Id (address), generate your "Access Token".
+ Edit `Qubic-AMD\appsettings.json`, change the "accessToken" to your own.
+ Run `Qubic-AMD\qli-Client.exe`.

### Skills

+ Run `qli-worker-gpu-amd-E139.exe AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA 0000000000000000000000000000000000000000000000000000000000000000 0 8` to test whether the algorithm kernel for AMD GPU can work properly.
+ The "cpuThreads" parameter in `appsettings.json` means the number of GPU Card you want to use.
+ Please do not change any parameters in `appsettings.json` except for "alias", "accessToken", "cpuThreads" and "LogLevel".
