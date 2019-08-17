# Vendor Flasher

The repo helps creating a zip to flash the vendor partition on A/B devices when provided a vendor.img
Useful when you have a device that requires using stock vendor and not a source built one.

## Instructions:
1. Extract the vendor.img from the ROM you want the vendor from, I suggest using https://github.com/cyxx/extract_android_ota_payload
2. Copy the vendor.img to the root of this repo
3. Edit the `testname` variable in META-INF/com/google/android/update-binary and any other print you want to modify
4. Time to zip it up, use 
   ```
   zip <name> -r *
   ```
   Example:
   ```
   zip enchilada-908-vendor -r *
   ```
5. You're done! Flash in TWRP or adb sideload it and you should be fine!
