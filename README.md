# Kogenta

A Kotlin native port of Google Magenta and Wave2Midi2Wave.

# Goals
## Port Google Magenta to Kotlin Native
Port Magenta to Kotlin Native to make it run on various platforms such as:
- iOS (arm32, arm64, emulator x86_64)
- MacOS (x86_64)
- Android (arm32, arm64)
- Windows (mingw x86_64)
- Linux (x86_64, arm32, MIPS, MIPS little endian)
- WebAssembly (wasm32)

## Add support for multipl GPUs
We will test with four Titan V cards to see how it scales well.

## Add support for Titan V tensor cores.
Figure out why the Python version of Magenta is running so slow during the training phase using Titan V. Modify TensorFlow if necessary to get the maximum 110 tflops performance from Titan V.

## Measure Performance
Measure the elapsed time during training of performance_rnn to see if we have any performance gains after porting Magenta to Kotlin Native.

# Milestones
## M1: performance_rnn - Basic
Port performance_rnn and dependent codes to Kotlin native.

## M2 : performance_rnn - Multiple GPUS
Add support for multiple GPUs to performance_rnn.

## M3 : performance_rnn - 110 tflops
Do performance tuning to get 110 tflops from a Titan V card during the training phase of performance_rnn.

## M4 : The MAESTRO Dataset loader
Write codes for loading the MAESTRO dataset in Kotlin native.
https://magenta.tensorflow.org/datasets/maestro

## M5 : Implement Wave2Midi2Wave
Reproduce Wave2Midi2Wave model in the following paper.

ENABLING FACTORIZED PIANO MUSIC MODELING AND GENERATION WITH THE MAESTRO DATASET
https://arxiv.org/abs/1810.12247

# Disclaimer
This is a personal project to learn about TensorFlow and Magenta. 
Not for a production usage.
I warned you ;-).