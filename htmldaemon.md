### Configure HTMLCOIN wallet for solo mining

* Go to [https://github.com/HTMLCOIN/HTMLCOIN/releases](https://github.com/HTMLCOIN/HTMLCOIN/releases)
* Download latest and install Windows win32-setup.exe
* Do not run HTMLCOIN yet
* Go to Start, Programs, HTMLCOIN, Right Click on HTMLCOIN, More, Open File Location
* Right click on HTMLCOIN shortcut, Properties, and edit Target
*  Add to the end of `htmlcoin-qt.exe` the following:
	*  `-server -rpcuser=user -rpcpassword=password -rpcport=4889 -rpcallowip=127.0.0.1`
* For Windows 64-bit, the target line should look like:
	* `"C:\Program Files (x86)\HTMLCOIN2\htmlcoin-qt.exe" -server -port=4888 -rpcport=4889 -rpcuser=user -rpcpassword=password -rpcallowip=127.0.0.1`

Now start HTMLCOIN QT wallet. This will sync the blockchain and act like a daemon for your miner at the same time.

Now download and configure a miner for [Nvidia CUDA](./nvidia.md) or [OpenCL (AMD/Intel)](./amd.md).