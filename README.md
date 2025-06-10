# gh-release-checker - GitHub Release Tracker

`gh-release-checker` is a Bash utility that tracks GitHub repository releases and notifies you when new versions become available. 

## Features ✨

- 🔔 Desktop notifications
- 📝 Simple configuration with plain text files

## Installation 💻

1. Clone this repository:
```bash
git clone https://github.com/chenxing-dev/gh-release-checker.git
cd gh-release-checker
```

2. Install dependencies:
```bash
sudo pacman -S curl jq libnotify
```

3. Make the script executable:
```bash
chmod +x gh-release-checker
```

## Configuration ⚙️

1. Edit the repositories file:
```bash
nano ~/.config/gh-release-checker/repos.conf
```

2. Add GitHub repositories in `owner/repo` format, one per line:

Example file:
```conf
torvalds/linux
neovim/neovim
```

## Why It Might Not Work 🔧

Here are common issues and solutions:

1. **Missing Dependencies**  
   Install required tools:
   ```bash
   sudo pacman -S curl jq libnotify
   ```

2. **GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown**  

   The error `GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown` occurs because your desktop environment doesn't have an active notification service running. 

   Install a Notification Daemon
   ```bash
   sudo pacman -S dunst libnotify
   dunst &
   ```

## Contributing 🤝

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a pull request

## License 📄

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.