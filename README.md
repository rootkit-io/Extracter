# Extracter

A lightweight bash utility for extracting common archive formats on Linux and Unix-like systems. Just pass a file and Extracter automatically detects the format and extracts it using the appropriate tool.

## Supported Formats

- **.tar** - tar archives
- **.tar.gz**, **.tgz** - gzip-compressed tar archives
- **.tar.bz2**, **.tbz2** - bzip2-compressed tar archives
- **.tar.xz**, **.txz** - xz-compressed tar archives
- **.gz** - gzip compressed files
- **.bz2** - bzip2 compressed files
- **.xz** - xz compressed files
- **.zip** - zip archives
- **.rar** - rar archives
- **.7z** - 7-zip archives
- **.tar.z** - old-style compressed tar

## Usage

```bash
./ext.sh file.tar.gz
```

Or add it to your `~/.bashrc` / `~/.zshrc` for global access:

```bash
alias ext='./ext.sh'
```

Then extract any archive with:

```bash
ext myfile.zip
```

## Installation

1. Download the script:
   ```bash
   curl -O https://raw.githubusercontent.com/rootkit-io/Extracter/main/ext.sh
   ```

2. Make it executable:
   ```bash
   chmod +x ext.sh
   ```

3. (Optional) Move it to your PATH:
   ```bash
   sudo mv ext.sh /usr/local/bin/ext
   ```

## Requirements

Make sure you have the necessary tools installed for the formats you want to extract:

- `tar` (usually pre-installed)
- `gzip` / `gunzip`
- `bzip2` / `bunzip2`
- `xz` / `unxz`
- `unzip`
- `unrar`
- `p7zip` / `7z`

On Debian/Ubuntu:
```bash
sudo apt install tar gzip bzip2 xz-utils unzip unrar p7zip-full
```

On Arch Linux:
```bash
sudo pacman -S tar gzip bzip2 xz unzip unrar p7zip
```

## License

MIT License - see [LICENSE](LICENSE) for details.
