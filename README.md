### Fonts that I can't afford to lose.

**Warning** : Linux brainlet ahead.

### Step - 1: Move the font binaries to the destination directory
  - copy the new fonts you want to install into the folder `~/.local/share/fonts` or `/usr/share/fonts`(for installing fonts globally)

### Step - 2: Clear and regenerate your font cache
```bash
fc-cache -f -v
```
- option f: force regenerate the cache for older font versions
- option v: verbose show the prodcedure of generating fonts

- fc-cache is used to build the font information cache files
- for more on it i would suggest to read the [man page of fc-cache](https://linux.die.net/man/1/fc-cache)

### Step - 3: Check if the fonts are properly installed
```bash
fc-list | grep JetBrainsMono | wc -l
```

### uninstalling fonts:
- Remove the font binaries from the respective folders (user fonts/ global fonts)
- Regenerate the font cache

---------------

#### More
- To see how production ready font installation scripts work look into this [**hacker font installation script**](https://gist.github.com/chrissimpkins/3b4b66d184476c7f20efb2e8f6435ff2#file-hack-linux-installer-sh)

