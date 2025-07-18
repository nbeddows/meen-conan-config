# MEEN Conan Config
General Conan configuration for any meen based project.
### Introduction
This project must be installed as a pre-requsite to building any meen based project.
### Install
To apply these profiles to your local environment:
`conan config install -sf profiles -tf profiles https://github.com/nbeddows/meen-conan-config.git`
### Profile customisation
To add a new profile, simply copy the profile that is the closest match to your new target profile and make and required changes, for example, creating a unity profile targeting Linux x86_64 gcc 14 would simply require you to copy the `Linux-x86_64-gcc-14-gtest` profile renaming the `gtest` framework portion of the file to `unity`. You may need to tweak the profile to suit your environment, in this case, remove all gtest specific options and add any required unity options. The same profile can be duplicated for any platform/architecture/compiler/version/framework combination simply by copying and renaming the profile with supported Conan values. In the case of pico sdk based profiles the platform name takes on one of the supported boards found [here](https://github.com/raspberrypi/pico-sdk/tree/master/src/boards/include/boards)