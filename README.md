# wsl-daemon

A simple, light weight daemon that monitors your WSL for malicious files, heavy CPU usage, suspicious connections, cleaning up temp files

## Setup

Clone the repo and make the script executable (it should already be):

```bash
chmod +x wsl-security-daemon
```

Optionally, move it somewhere in your PATH:

```bash
sudo cp wsl-security-daemon /usr/local/bin/
```

## Usage

Start the daemon:

```bash
./wsl-security-daemon start
```

Check status:

```bash
./wsl-security-daemon status
```

Run a quick scan:

```bash
./wsl-security-daemon scan
```

For real-time file monitoring, you'll need inotify-tools:

```bash
./wsl-security-daemon rt-install
./wsl-security-daemon rt-start
```

For antivirus scanning with ClamAV:

```bash
./wsl-security-daemon av-install
./wsl-security-daemon av-update
```

See all commands:

```bash
./wsl-security-daemon help
```
