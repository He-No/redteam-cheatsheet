### bruteforce targeted
hashcat -m <hashmode> -a <attackType> -o <outputFile> (--remove) <hashFile> <wordlist> --force --show

### bruteforce mode
hashcat -m <hashMode> -o <outputFile> <hashFile> <dictionary> --force

### generate wordlist
hashcat --stdout -a <attackType> <charsets> | tee <outFile>