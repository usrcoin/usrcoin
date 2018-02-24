# Guide build by hongbaocoin developer

Source install instructions && make:

Ubuntu 14:

git clone https://github.com/FndNur1Labs/CryptonoteEvo.git
cd cryptonoteevo
./install.sh --wait for dependencies to finish
make --type make in terminal for cmake to compile
finished - daemon is saved in cryptonoteevo/build/release/src/ cryptonoted

Windows 10 64bit:

hit windows key search “windows update settings”. Left hand side click “for developers” then check “developer mode”. Wait for install to finish. Then you can close “windows update settings”
hit windows key go to: “Control Panel\Programs” click “turn windows feature on and off” next check “windows subsystem for linux” after restart your computer
download: https://www.microsoft.com/store/productId/9NBLGGH4MSV6
hit windows key and search “ubuntu” open program install will automatically happen then create user name and password
type “apt update” wait for updates to finish
type “apt install git” wait for install to finish
type “git clone https://github.com/FndNur1Labs/CryptonoteEvo.git“
type “cd hongbao”
type “./install.sh” wait for dependency installation to finish it takes a little time.
type "make" and wait for cmake to compile for you this also takes some time
finished - daemon is saved in cryptonoteevo/build/release/src/ cryptonoted

Basic commands to start mining:

Run in this order ./evowallet ./cryptonoted ./miner

VERY IMPORTANT !!!!!! DONT EVER CLOSE YOUR WALLET WITH CNTRL C OR CLICKING X. YOU MUST TYPE "save" OR YOUR COINS WILL NOT BE SAVED!!!!!!!!!!!!!!!

"cd build/release/src && ./evowallet" – this runs your wallet. When you first run you can generate a new wallet by typing “g” and follow instructions. 
After you typed "save" and closed your wallet you can use the following command to open it again "cd cryptonoteevo/build/release/src && ./evowallet --wallet-file name.wallet" note name.wallet is the name you gave your wallet when you created it. for more command you can use "./simplewallet --help"


You need to open another ubuntu terminal. 
If on Windows 10 right click icon launcher and open another ubuntu terminal. 

"cd cryptonoteevo/build/release/src && ./cryptonoted" – runs daemon this is required to be ran every time to connect to the network. WHEN CLOSING REMEMBER TO TYPE “exit” SO YOUR SYNC SAVES.

You need to open another ubuntu terminal. 
If on Windows 10 right click icon launcher and open another ubuntu terminal.


You cannot mine from within your wallet you will need to open another terminal and “cd cryptonoteevo/build/release/src && ./miner –address yourwalletaddress –log-level 5” note yourwalletaddress is your wallets address. You can find this address when you run simplewallet. To stop mining you can use ctrl c or click x. Note be very careful your not closing your wallet with out save command!!! Check twice so you know what you are closing 100%.

If for any reason you have an issueing opening your evowallet the second time please use this command to run it "./evowallet --command reset --wallet-file yourwalletname"


