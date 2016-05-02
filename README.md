# WarpWallet Cracker
A very, very basic WarpWallet cracker that can optionally use an insight-api server to check the wallets of each
address it loops over. Does *not* test that it has already checked an address before. It is extremely unlikely you will
actually manage to crack an address using this (or even find a wallet with money in)

FWIW: You should not steal money from wallets you find. Do NOT use this tool for malicious reasons. Solely made for
education.

Keybase have some nice little challenges for WarpWallet cracking. You can see some of the active challenges here:
https://keybase.io/warp - as of 2nd May 2016 there is currently a challenge for 20 BTC (worth $8927.80 at the time of
writing)

This is by no means optimised and just serves as a proof of concept for some ideas I have for the future. I currently
have this sitting on an idle server I had, it's not costing me any more money and who knows - one of us might actually
brute force it one day.

If you wanted to optimise this, I'd recommend writing it in something more low level (obviously not something that runs
in a VM) and take advantage NVIDIA's CUDA cores.

Syntax:

    # [address to crack] [salt] [insight api to use - or "0"]
    java -jar target/WarpWallet-1.0-SNAPSHOT-jar-with-dependencies.jar 1AdU3EcimMFN7JLJtceSyrmFYE3gF5ZnGj a@b.c "http://91.121.83.82:3001/insight-api"

Remember to build the project before running it. `mvn install`