#Setting up a minimal tree for building TWRP
##Android 6.0 branch
This repo is ~5.0GB
###To initialize the main repository:

````
repo init -u https://github.com/eagleeyetom/recovery_manifest.git -b android-6.0
````
Then add any recovery/device trees/kernels you need to a file (one XML for each device) and add them to the .repo/local_manifests folder of your initialized repo folder.

Once added:
````
repo sync
````
Done

To build recovery:
````
. build/envsetup.sh
lunch (devicename)
make installclean
time make recoveryimage
````

###Credits go to marduk191
