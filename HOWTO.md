# How to Setup the Environment and Run

*Author: Yue Lyu*

This step by step tutorial is only available for MacOS now.

## Software to Install

1. XCode 13
1. VST SDK, [link](https://github.com/steinbergmedia/vst3sdk#500)
1. Bitwig Studio, [link](https://www.bitwig.com/download/)
1. BrainCo python SDK, [link](https://focus-resource.oss-accelerate-overseas.aliyuncs.com/universal/crimson-sdk-prebuild/1.1.0/python/python.zip)

## Dependencies to Install

## Build and Deploy the Plugin

## Start the application

1. Start BrainCo headband python sdk, connect the band via Bluetooth so that the eeg information will be transmitted to your laptop and saved in a file for further process.

1. Start process_eeg.py or dqn.py, which will process the raw eeg data saved in the file mentioned in the above step and output the result data into another file. This might be done in a Docker which runs Ubuntu image, b/c some of the machine learning dependencies might NOT work in MacOS.

1. Now start the Bitwig Studio and load the plugin that we build in the previous section. Choose a audio file and play. Please note, the plugin will read the processed data from the file generated in the above step, and then modify the output of the audio file.

1. Start swimulator.py under SWIM folder, it will bring up a GUI in which curves change along with the music.