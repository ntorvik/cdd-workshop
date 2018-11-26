## Setup toolchain for ESP32

1. In the Cloud9 Terminal window install prerequisites

```bash
sudo yum install flex gperf
```
```bash
sudo pip install argparse cryptography serial
```

2. Download 64-bit version of Xtensa ESP32 toolchain:

```bash
cd ~/environment
wget https://dl.espressif.com/dl/xtensa-esp32-elf-linux64-1.22.0-80-g6c4433a-5.2.0.tar.gz
```

3. Create *esp* directory and unzip the tar archive there:

```bash
mkdir ~/environment/esp
cd ~/environment/esp
tar xvfz ../xtensa-esp32-elf-linux64-1.22.0-80-g6c4433a-5.2.0.tar.gz
```

4. Add toolchain path to *~/.bash_profile* PATH variable

```bash
PATH=$PATH:$HOME/.local/bin:$HOME/bin:$HOME/environment/esp/xtensa-esp32-elf/bin
```

5. Re-evaluate ~/bash_profile

```bash
source ~/.bash_profile
```
