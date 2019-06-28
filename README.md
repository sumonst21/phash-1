# pHash&trade; Perceptual Hashing Library

pHash is a collection of perceptual hashing algorithms for image,
audo, video and text media.  

## Installation

Build and install like so:

```
cd <project-dir>
cmake .
make
sudo make install
```

The build can exclude various hashing algorithms by passing
the variables USE_IMAGE_HASH, USE_AUDIO_HASH, USE_VIDEO_HASH
OR USE_TEXT_HASH to cmake program: `cmake -DUSE_IMAGE_HASH=1`


## Image Hashing

There are four image hash algorithms in the pHash librarie.

1. DCT image hash
   A 64-bit binary hash based on the global discrete cosine transform (dct)
   of the image.  Comparisons are made by calculating the hamming distance,
   or the number of places where the bits differ, between two hashes.

2. Radial Image Hash
   A perceptual hash based on the variances of pixels taken from strips of
   various angles across the center of the image.
   
3. MH Image hash
   Based on the mexican hast wavelet function.
   
4. BMB Image Hash - Box-Mean-Binarized Hash
   The image is divided up into 16x16 pixel-sized boxes.  The
   mean value is calculated for each box in the gird, and a binarized
   hash is formed based on each mean value with respect to the median
   of those mean values. A basic hamming distance is used to compute
   distances.

## Audio Hash

An audio hash is included here for completeness.  There is a fuller java
implementation here: [JPHashAudio](https://github.com/starkdg/JPhashAudio)

## Video Hash

A video hash is included.  A fuller c++ implementation is available
here: [ClipSeekr](https://github.com/starkdg/clipseekr)

## Text Hash




## Requirements for Example Programs

Boost 1.70.0 - Only the filesystem, system and program_options libraries.


## Requirements for Image Hash

CImg v.6.6 (included)
libtiff-dev (optional)
libpng-dev (optional)
libjpeg-dev (optional)


## Requirements for Video Hash

ffmpeg v2.8.15 "feynman release" 
  libavformat
  libavcodec
  libavswscale

## Requirements for Audio Hash

libsndfile v1.0.27
libsamplerate v0.1.8
libmpg123 v1.23.8 (optional)
libvorbis v1.3.5 (optional)
libogg v1.3.2 (optional)

