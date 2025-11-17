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
