# Bash scripts
This folder contain scripts to ease life while developing on Android.

## ./_config_apps.sh
This script set the list of the applications that must be used by other scrips (clear_data_app.sh, ...).

## ./_config_signatures.sh
This script define the expected signature of the applications
- signatureListArray : the signatures.
- certificateHashArray : the certificates hashes.
- signatureAPKNameExceptionArray : the list of the APKs that the signature must be ignored.

## ./_generic_methods.sh
This script contain generic functions used by other scripts.

### detect_os
Based on different methods, try to get the OS type we are running on.

### detect_os_uname
Used by detect_os when the first method fail, to detect the OS.

### wait_for_device
Wait for any Android device to be connected.

### pushd and popd
Avoid displaying stack when using popd and pushd

### check_java
Check that Java is available.

### check_adb
Check that ADB is available.

### 
Check that zipalign is available.

### check_aapt
Check that aapt is available.

### check_certutil
Check that certutil is available.

### check_jarsigner
Check that jarsigner is available.

### check_emulator
Check that emulator is available.

### check_keytool
Check that keytool is available.

### check_telnet
Check that telnet is available (For Windows).

### check_python
Check that python is available (For Windows).

### check_pip
Check that pip is available (For Windows).

### check_frida
Check that frida is available (For Windows).

## ./_template_serial.sh
This is a template for script using serial name.

## ./_template_serial_package.sh
This is a template for script using serial name AND package name.

## ./activate_connect_tcp.sh
This script activate Wi-Fi, then activate ADB over Wi-Fi, extract IP address and connect to device.


Example : 
```sh
./activate_connect_tcp.sh
./activate_connect_tcp.sh -s emulator-5556
```

## ./alarm_test.sh
This script display the next alarm set for an application.


Example : 
```sh
./alarm_test.sh
./alarm_test.sh -s emulator-5556
```

## ./battery_optimization.sh
This script add or remove the application to the battery optimization list.


Example : 
```sh
./battery_optimization.sh -p com.android.vending
./battery_optimization.sh -s emulator-5556 -p com.android.vending
./battery_optimization.sh -s emulator-5556 -p com.android.vending -r
./battery_optimization.sh -s emulator-5556 -p com.android.vending -r -d
```

## ./bucket_level.sh
This script display the bucket level of an application.
More information here : https://developer.android.com/topic/performance/appstandby


Example : 
```sh
./bucket_level.sh -p com.android.vending
./bucket_level.sh -s emulator-5556 -p com.android.vending
```

## ./calc_hash_folder.sh
This script calculate the hash of all the APKs located in the folder passed in parameter.
You can use it with the script calc_hash_device.sh that do the same, but with applications located and extracted from a device.


Example : 
```sh
./calc_hash_folder.sh /c/apk/
```

## ./change_ui_mode_light.sh
This script activate the UI Light mode.

Example : 
```sh
./change_ui_mode_light.sh
./change_ui_mode_light.sh -s emulator-5556
```

## ./change_ui_mode_night.sh
This script activate the UI Night mode.

Example : 
```sh
./change_ui_mode_night.sh
./change_ui_mode_night.sh -s emulator-5556
```

## ./check_apps_state.sh
This script give a status of the applications listed in the _config_apps.sh script:
- Installed or NOT.
- DEBUG/RELEASE mode.
- Backupable or NOT.  


Example : 
```sh
./check_apps_state.sh
```

## ./choose_device.sh
This script allow to run other script on a chosen device or on all connected devices.


Example : 
```sh
./choose_device.sh
```

## ./choose_device_and_package.sh
This script allow to run other script on a chosen device or on all connected devices, and if on one device you can choose the package.


Example : 
```sh
./choose_device_and_package.sh
```

## ./choose_device_usb.sh
This script allow to run other script on a chosen device or on all connected devices.


Example : 
```sh
./choose_device.sh
```

## ./choose_package.sh
This script allow to run other script and select the package in installed applications on device.
Note: Works only if one device is connected. Use choose_device_and_package.sh script if more than one device is connected.


Example : 
```sh
./choose_package.sh
```
This script clear the application data.

## ./clear_app.sh
This script clear the application data.


Example : 
```sh
./clear_app.sh -p com.android.vending
./clear_app.sh -s emulator-5556 -p com.android.vending
```

## ./clear_data_apps.sh
This script clean the applications that are in the _config_apps.sh script.


Example : 
```sh
./clear_data_apps.sh
./clear_data_apps.sh -s emulator-5556
```

## ./close_apps.sh
This script close the applications that are in the list of _config_apps.sh script.


Example : 
```sh
./close_apps.sh
./close_apps.sh -s emulator-5556
```

## ./delete_all_apps.sh
This script delete all the applications of the list defined in _config_apps.sh script.


Example : 
```sh
./delete_all_apps.sh
./delete_all_apps.sh -s emulator-5556
```

## ./delete_app.sh
This script delete the application in parameter. Use with choose_package.sh to get the name of the package.


Example : 
```sh
./delete_app.sh -p com.android.vending
./delete_app.sh -s emulator-5556 -p com.android.vending
```

## ./dev_light4events.sh

## ./device_info.sh
This script display some information about the device.


Example : 
```sh
./device_info.sh
./device_info.sh -s emulator-5556
```

## ./enter_doze_mode.sh
This script contain an example to update the password of the keystore and the KeyAlias.


Example : 
```sh
./keystore_password.sh
```

## ./lockito.sh

