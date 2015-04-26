Read the original README.md at README-ORIGINAL.md

This is a dirty branch to make JNA work on Android while still using Gradle.

Instructions:

    git clone
    cd jna
    ant -Dos.prefix=android-arm dist
    go to /dist, copy jna.jar on your project's libs folder
    while in dist, open android-arm.jar with an archiver like 7Zip
    extract libjnidispatch.so to a temporary folder
    create a folder on your projects as /src/main/jniLibs/armeabi
    move libjnidispatch.so to that directory
    repeat for android-x86 and /src/main/jniLibs/x86
    OPTIONAL: for armeabi-v7a try using the same .so as in ameabi