---
description: Installing dependencies and setting up your theos environment
---

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

{% code-tabs %}
{% code-tabs-item title="Installing dependencies with Homebrew" %}
```bash
brew install ldid xz dpkg
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Next, set up your THEOS ****environment ****variable by pasting this command:

{% code-tabs %}
{% code-tabs-item title="Adding $THEOS to your bash profile" %}
```bash
echo "export THEOS=~/theos" >> ~/.profile
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Let's clone the Theos repository to the folder we just created:

{% code-tabs %}
{% code-tabs-item title="Cloning the git repository" %}
```bash
git clone --recursive https://github.com/theos/theos.git $THEOS
```
{% endcode-tabs-item %}
{% endcode-tabs %}

You can grab the latest iOS SDKS by pasting the next two commands:

{% code-tabs %}
{% code-tabs-item title="Downloading the ZIP archive" %}
```text
curl -LO https://github.com/theos/sdks/archive/master.zip
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Extracting the contents to the sdks folder" %}
```text
unzip master.zip -d $THEOS/sdks
```
{% endcode-tabs-item %}
{% endcode-tabs %}

To finish the installation, set up a ghostbin script:

{% code-tabs %}
{% code-tabs-item title="Adding the ghost.sh script" %}
```bash
curl https://ghostbin.com/ghost.sh -o $THEOS/bin/ghost
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Giving permissions to the file" %}
```bash
chmod +x $THEOS/bin/ghost
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Windows/Linux Installation

### Software Prerequisites

#### Windows: 

* Windows Subsystem for Linux

{% hint style="info" %}
Targets: **iOS**, **Linux**
{% endhint %}

#### - Windows/Linux:

Add the correct _clang-6.0 source_ for your Linux distro. Instructions can be found [here](http://apt.llvm.org/).

{% code-tabs %}
{% code-tabs-item title="Refreshing sources" %}
```bash
sudo apt-get update
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Next, paste the following command:

{% code-tabs %}
{% code-tabs-item title="Installing dependencies" %}
```bash
sudo apt-get install fakeroot git perl clang-6.0 build-essential
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Next, set up your THEOS ****environment ****variable by pasting this command:

{% code-tabs %}
{% code-tabs-item title="Adding $THEOS to your bash profile" %}
```bash
echo "export THEOS=~/theos" >> ~/.profile
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Let's clone the Theos repository to the folder we just created:

{% code-tabs %}
{% code-tabs-item title="Cloning the git repository" %}
```bash
git clone --recursive https://github.com/theos/theos.git $THEOS
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Next, we need the iOS toolchain. Paste the following commands, one by one:

{% code-tabs %}
{% code-tabs-item title="Downloading the toolchain" %}
```bash
curl https://kabiroberai.com/toolchain/download.php?toolchain=ios-linux -Lo toolchain.tar.gz 
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Extracting the contents to the toolchain folder" %}
```bash
tar xzf toolchain.tar.gz -C $THEOS/toolchain
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Removing the downloaded archive" %}
```bash
rm toolchain.tar.gz
```
{% endcode-tabs-item %}
{% endcode-tabs %}

You can grab the latest iOS SDKS by pasting the next two commands:

{% code-tabs %}
{% code-tabs-item title="Downloading the ZIP archive" %}
```text
curl -LO https://github.com/theos/sdks/archive/master.zip
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Extracting the contents to the sdks folder" %}
```text
unzip master.zip -d $THEOS/sdks
```
{% endcode-tabs-item %}
{% endcode-tabs %}

To finish the installation, set up a ghostbin script:

{% code-tabs %}
{% code-tabs-item title="Adding the ghost.sh script" %}
```bash
curl https://ghostbin.com/ghost.sh -o $THEOS/bin/ghost
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Giving permissions to the file" %}
```bash
chmod +x $THEOS/bin/ghost
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Other Installations

### iOS Installation

I placed the iOS installation as an _Other Installation_, as it seems impractical to use when writing a tweak. Tweak development includes debugging and disassembly at times, and \(for the most part\) these are not available on iOS.

#### Software Prerequisites

* Jailbroken iOS Device
* Cydia

Open Cydia and add the following sources**:**

* [https://coolstar.org/publicrepo](https://coolstar.org/publicrepo)
* [http://repo.bingner.com/](http://repo.bingner.com/) 

After adding the repos, search for _Theos Dependencies_ and install the package from the [BigBoss](https://apt.thebigboss.org/repofiles/cydia) repo.



![](.gitbook/assets/screen-shot-2018-10-27-at-3.25.49-pm.png)

![Installing the Dependencies will take time to complete](.gitbook/assets/screen-shot-2018-10-27-at-3.27.22-pm.png)

Next, set up your THEOS ****environment ****variable by pasting this command in a Terminal:

{% code-tabs %}
{% code-tabs-item title="Adding $THEOS to your bash profile" %}
```bash
echo "export THEOS=~/theos" >> ~/.profile
```
{% endcode-tabs-item %}
{% endcode-tabs %}

![](.gitbook/assets/screen-shot-2018-10-27-at-3.37.50-pm.png)

Let's clone the Theos repository to the folder we just created:

{% code-tabs %}
{% code-tabs-item title="Cloning the git repository" %}
```bash
git clone --recursive https://github.com/theos/theos.git $THEOS
```
{% endcode-tabs-item %}
{% endcode-tabs %}

You can grab the latest iOS SDKS by pasting the next two commands:

{% code-tabs %}
{% code-tabs-item title="Downloading the ZIP archive" %}
```text
curl -LO https://github.com/theos/sdks/archive/master.zip
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Extracting the contents to the sdks folder" %}
```text
unzip master.zip -d $THEOS/sdks
```
{% endcode-tabs-item %}
{% endcode-tabs %}

To finish the installation, set up a ghostbin script:

{% code-tabs %}
{% code-tabs-item title="Adding the ghost.sh script" %}
```bash
curl https://ghostbin.com/ghost.sh -o $THEOS/bin/ghost
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="Giving permissions to the file" %}
```bash
chmod +x $THEOS/bin/ghost
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## **Troubleshooting**

### Installing with zsh

* If you are using zsh, `echo "export THEOS=~/theos" >> ~/.profile` will not work because you are applying this to your bash profile rather than the zsh one.
* **Paste the following command to add the $THEOS location to zsh**:

```bash
echo "export THEOS=~/theos" >> ~/.zprofile
```



