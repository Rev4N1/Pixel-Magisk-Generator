# Pixel-Magisk-Generator
This is an automated repository that creates magisk-patched images for pixel devices.

### Disclaimer

**Use at your own risk!!** I am not responsible for whatever you do with your device. 

### How-to steps

1. Open [image_info.json](./image_info.json) and edit as you like. Required info can be found at [Google's Factory Images](https://developers.google.com/android/images)

   * `name`: The device codename.
   * `build_number`: The build number.
   * `link`: Factory Image direct download link.
   * `checksum`: Factory Image checksum.
   * `magisk`: Magisk apk direct download link.

2. Connect your phone and get output from `adb shell getprop`.

   You don't need all the values. You only need these values:

   * `ro.crypto.state`
   * `ro.build.ab_update`
   * `ro.boot.slot_suffix`
   * `ro.build.version.sdk`
   * `ro.product.cpu.abi`

3.  Open [GETPROP_OUTPUT](./GETPROP_OUTPUT) and edit with the values you got above.

4. Wait 5 minutes, and you will have your patched image and the original image in releases tab!