---
layout: post
title:  "Audio Encoding"
date:   2015-08-30 11:23:32
categories: audio
---
#A introduction to basic audio encoding
There are many different kinds of audio codecs. The main ones I will go over are: `.aiff` `.wav` `.aac` `.mp3` `.wma` `.ogg` (vorbis) `.opus` `.m4a` (apple lossless, alac) `.flac` .
There are two main groups based on the compression algorithm they implement. 
Audio storage has come a long way from the first phonograph, digital media has over-taken analogue.
However, with current advances in both encoding and playback, there is very little difference left.
The two major types of compression are lossy and lossless. As the names imply, with lossy compression you lose (theoretically imperceivable) data to save space.
With lossless, you save every bit of data you can while still using strong compression to save on storage space.

| Lossless    | Lossy |
|:-------------   |:------------- |
| `.m4a` (alac)    | `.mp3`  |
| `.flac`    | `.aac`  | 
| `.wav` *   | `.opus` | 
| `.aiff`*	  | `.wma` |
|			  | `.ogg` (vorbis) |

>`.wav` and `.aiff` are interesting cases because they could be either lossy or lossless. 
They are the uncompressed formats, `.wav` in windows and `.aiff` in mac os x, and for most purposes considered raw pcm (pulse-code modulation) containers.
The problem comes from the fact that there is no way to know the source that the files were created from. 
I could decompress an `.mp3` which clearly was previously compressed using a lossy algorithm. 
The resulting file would technically be "uncompressed" but this does not mean I would get the same raw pcm stream back.

An easy way to see lossy vs lossless is to plot the spectrogram of the file you are working with.
I personally use [spek](http://spek.cc/) , an open-source project based on the ffmpeg libraries, with simple drag and drop support.
Here's a sample lossless spectrogram:

![.flac spectrogram](https://raw.githubusercontent.com/knaik94/knaik94.github.io/master/images/spek1.JPG)
[for more info about spectrograms](https://en.wikipedia.org/wiki/Spectrogram)





 
