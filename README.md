platform_manifest
=================

manifest used for syncing repos.

$ repo init -u https://github.com/TeamBAMF/platform_manifest.git

$ repo sync

$ cd vendor/<manufacturer>/<device> (for example: 'cd vendor/samsung/toro')

$ chmod a+x build-vendor.sh

Plug your phone into the PC at this time and make sure adb recoginzes it.  We're going to grab some files.

$ ./build-vendor.sh

You should see a bunch of files being pulled off your phone.  If you get a couple errors, don't stress it.  There are some files that may not be there.  If you get a lot of errors, freak out.

$ cd ../../../

$ make clean && source build/envsetup.sh && <your lunch command here> && time make -j9 otapackage

Lunch commands:
VZW Nexus - 'lunch bamf_nexus-userdebug'
GSM Nexus - 'lunch bamf_maguronexus-userdebug'
Sprint Nexus - 'lunch bamf_nexus_spr-userdebug'
Galaxy Nexus 7 - 'lunch bamf_grouper-userdebug'


If all goes well, you should have a freshly compiled copy of BAMF Paradigm when you are done.  If you encounter any problems, hit us up on the forums at TeamBAMF.net.  We aren't really supporting unofficial builds, but we'll help where we can. :)
