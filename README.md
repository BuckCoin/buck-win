# Buck - The Future of Cryptocurrency
For more details check root [Buck repository](https://github.com/buckcoin/buck) 

### Windows

Prerequisites:
```{r, engine='bash'}
# Download this file:
https://z.cash/downloads/sprout-proving.key
# Download this file:
https://z.cash/downloads/sprout-verifying.key
# Create an new directory in this excat location: 
mkdir “%HOMEPATH%\AppData\Roaming\ZcashParams
# Move the two downloaded files to the <ZcashParams> directory
```

- Download Windows release binary [here](https://github.com/buckcoin/buck-win/releases)

Download the windows exe files, place them in a directory, then:
```{r, engine='bash'}
# How to start Buck for the first time
# Open a CMD window
# Within the CMD window
cd [c:/[Directory_With_EXE_Files]
# Run Buck for the first time
Zcashd
# Buck will provide you with instructions on how to modify the buck.conf file
# Create a new file named buck.conf in the directory specified 
# Insert the following into the new buck.conf file 
addnode=159.89.40.161
addnode=139.59.111.53
addnode=45.55.195.233
addnode=138.68.95.165
addnode=18.216.125.20
addnode=54.211.59.227
addnode=104.31.64.31
addnode=104.27.142.97
addnode=142.44.143.182
addnode=80.211.255.12
addnode=18.194.142.46
addnode=89.47.163.190
addnode=35.194.186.70
# Save the buck.conf file
# In a CMD window start Buck again (from the [c:/[Directory_With_EXE_Files])
Zcashd
# The node will download blocks. You are now running a Buck node and wallet!
# Leave the main CMD window open, and open another window to run zcash-cli wallet commands
```

- or - 

- Build binaries on your own from scratch (tested in Ubuntu 16.04)
Get dependencies
```{r, engine='bash'}
sudo apt-get install \
      build-essential pkg-config libc6-dev m4 g++-multilib \
      autoconf libtool ncurses-dev unzip git python \
      zlib1g-dev wget bsdmainutils automake mingw-w64
```

Install (Cross-Compiled, building on Windows is not supported yet)
```{r, engine='bash'}
# Build
./zcutil/build-win.sh --disable-rust -j$(nproc)
```
The exe will save to `src` which you can then move to a windows machine

Security Warnings
-----------------

**Buck is experimental and a work-in-progress.** Use at your own risk.
