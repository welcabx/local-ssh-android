# SSH into your Android Locally
Turn your Android device to a local SSH server using *Termux*. This is my personal guide to connect to my Android from my laptop within the same network.

> Termux should be already installed on your Android.

1. **Install Termux Packages**
```bash
pkg update && pkg upgrade
```
```bash
pkg install openssh
```

2. **Set Password for SSH**
```bash
passwd
```

3. **Start the SSH Server**
```bash
sshd
```
> By default, it listens on port **8022**

4. **Get your Android's local IP and user ID**  
Local IP:
```bash
ifconfig
```
> Your device local IP is after the 'inet' and starts with '192.168.xx.xx'

user ID:
```bash
whoami
```
> It starts with 'u0_axxx'

5. **SSH from your Laptop or PC**
```bash
ssh -p 8022 *userID*@*AndroidIP*
```
> Enter the ssh password your created before on your Android.

**You should see a 'Welcome to Termux' screen once you successfully SSH to your Android!**

### Support
If you find this useful, Don't forget to star the repo!
