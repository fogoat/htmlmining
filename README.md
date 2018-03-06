# htmlmining
# Unofficial HTMLCOIN Mining Group

### [GPU Hash Rates](./hashrate/htmlcoin-gpu-hashrates.md)

### [Frequently Asked Questions](./FAQ.md)

### Solo Mining HTMLCOIN via GPU (Nvidia & AMD)

### 

## NVIDIA CUDA

* Go to [https://github.com/HTMLCOIN/HTMLCOIN/releases](https://github.com/HTMLCOIN/HTMLCOIN/releases)
* Download latest and install Windows win32-setup.exe
* Do not run HTMLCOIN yet
* Go to Start, Programs, HTMLCOIN, Right Click on HTMLCOIN, More, Open File Location
* Right click on HTMLCOIN shortcut, Properties, and edit Target
*  Add to the end of `htmlcoin-qt.exe` the following:  `-server -rpcuser=user -rpcpassword=password -rpcport=4889 -rpcallowip=127.0.0.1`
* For Windows 64-bit, the target line should look like: `"C:\Program Files (x86)\HTMLCOIN2\htmlcoin-qt.exe" -server -port=4888 -rpcport=4889 -rpcuser=user -rpcpassword=password -rpcallowip=127.0.0.1`

Now start HTMLCOIN QT wallet. This will sync the blockchain and act like a daemon for your miner at the same time.

Once running, get ccminer from mghtthr: [https://github.com/mghtthr/ccminer](https://github.com/mghtthr/ccminer)

You must compile yourself at this time.

To solo mine, run this ccminer command:
`ccminer.exe -a htmlcoin -o http://127.0.0.1:4889 -u user -p password --no-stratum`

If you get *invalid device symbol*, your GPU is too old. Try bfgminer with OpenCL instead.

## OpenCL (AMD, Intel)

You have to compile bfgminer [https://github.com/johninaustin/](https://github.com/johninaustin/) yourself.

cryptojoeholder created a Windows binary for us [https://github.com/cryptojoehodler/bfgminer-32bit-html/releases/tag/bfgminer-html-2.0.2-AMD](https://github.com/cryptojoehodler/bfgminer-32bit-html/releases/tag/bfgminer-html-2.0.2-AMD).

To solo mine:  
`bfgminer -S opencl:auto -o http://localhost:4889 -u user -p password --no-gbt`

## Pool Mining

[https://html.mineto.site/index.php](https://html.mineto.site/index.php)

[https://html.mineto.site/index.php?page=gettingstarted](https://html.mineto.site/index.php?page=gettingstarted)

modifed ccminer for Windows: [https://drive.google.com/file/d/1nAM80H6PLA_vMuYEBo6gFZQQrDc5a7Hr/view?usp=sharing](https://drive.google.com/file/d/1nAM80H6PLA_vMuYEBo6gFZQQrDc5a7Hr/view?usp=sharing)

You must use this custom binary to mine with this pool.