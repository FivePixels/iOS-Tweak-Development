# Theos Installation

## macOS Installation

### Software Prerequisites

* OS X 10.9 \(Mavericks\)
* [Homebrew](https://brew.sh) 
* [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) $$^1$$ 

$$^1$$ Xcode 5.0 or newer is required.

{% hint style="info" %}
Targets: **macOS**, **iOS**, **tvOS**, **watchOS**
{% endhint %}

### Installation

Open **Terminal.app** and paste the following command:

```bash
brew install ldid xz
```

Next, set up your THEOS ****environment ****variable by pasting this command:

```bash
echo "export THEOS=~/theos" >> ~/.profile
```

Let's clone the Theos repository to the folder we just created:

```bash
git clone --recursive https://github.com/theos/theos.git $THEOS
```

Download the following [repo](https://github.com/theos/sdks) as a ZIP archive and extract the contents into a folder. Select and copy the .sdk files you plan on building for in the $THEOS/sdks folder.

To finish the installation, set up a ghostbin script:

```bash
curl https://ghostbin.com/ghost.sh -o $THEOS/bin/ghost
```

```bash
chmod +x $THEOS/bin/ghost
```



