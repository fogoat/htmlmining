### Solo Mining HTMLCOIN via AMD GPU

![OpenCL](./images/intel-amd.jpg)

First configure [HTMLCOIN wallet for solo mining](./html-daemon.md)

You have to compile bfgminer [https://github.com/johninaustin/](https://github.com/johninaustin/) yourself.

cryptojoeholder created a Windows binary for us [https://github.com/cryptojoehodler/bfgminer-32bit-html/releases/tag/bfgminer-html-2.0.2-AMD](https://github.com/cryptojoehodler/bfgminer-32bit-html/releases/tag/bfgminer-html-2.0.2-AMD).

To solo mine:  
`bfgminer -S opencl:auto -o http://localhost:4889 -u user -p password --no-gbt`