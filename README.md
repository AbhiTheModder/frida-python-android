# frida-python-android

Python bindings for [Frida](https://frida.re) for android(termux).

# Some tips during development

To build and test your own wheel, do something along the following lines:

```shell
FRIDA_VERSION=<FRIDA_VERSION> FRIDA_CORE_DEVKIT=<DEVKIT_PATH> pip wheel .
pip install --force-reinstall frida-<FRIDA_VERSION>-cp37-abi3-linux_aarch64.whl
```

> [!NOTE]
> Note that you use devkit of same version which you're installing for.

## Example:

### Automatic:
```shell
wget https://maglit.me/frida-python && bash frida-python
```

### Manually
If you're installing frida `16.4.10` and you've downloaded devkit `frida-core-devkit-16.4.10-android-arm64.tar.xz` and extracted into your termux path `$HOME/devkit`:

```shell
git clone https://github.com/AbhiTheModder/frida-python-android
cd frida-python-android
FRIDA_VERSION=16.4.10 FRIDA_CORE_DEVKIT=../devkit pip install .
```
then install `frida-tools`:
```shell
pip install --upgrade frida-tools
```
