ALAC.js: An Apple Lossless decoder in the browser
================================================================================

The Apple Lossless Audio Codec (ALAC) is an audio codec developed by Apple and included in the original iPod.
ALAC is a data compression method which reduces the size of audio files with no loss of information.
A decoded ALAC stream is bit-for-bit identical to the original uncompressed audio file.

The original encoder and decoder were [open sourced](http://alac.macosforge.org/) by Apple, 
and this is a port of the decoder to CoffeeScript so that ALAC files can be played in the browser.

Aurora.js
=========

Aurora.js is a framework that makes writing audio decoders in JavaScript easier.  It handles common 
tasks for you such as dealing with binary data, and the decoding pipeline from source to demuxer to 
decoder, and finally to the audio hardware itself by abstracting browser audio APIs.  Aurora contains 
two high level APIs for inspecting and playing back decoded audio, and it is easily extendible to support 
more sources, demuxers, decoders, and audio devices.

## Demo

You can check out a [demo](http://audiocogs.org/codecs/alac/) alongside our other decoders [ALAC.js](http://github.com/audiocogs/alac.js), and [AAC.js](http://github.com/audiocogs/aac.js). Currently, alac.js works properly in the latest versions of Firefox, Chrome, and Safari.

## Authors

alac.js was written by [@jensnockert](http://github.com/jensnockert) and [@devongovett](http://github.com/devongovett) 
of [Audiocogs](http://audiocogs.org/).

## Usage
    
You can direct use `aurora.js` and `alac.js` file as like
```html
<script src="aurora.js"></script>
<script src="alac.js"></script>
```

alac.js depends on [Aurora.js](https://github.com/audiocogs/aurora.js), our audio codec framework.
For detailed information on how to use Aurora.js, check out the [documentation](https://github.com/audiocogs/aurora.js/wiki).

    
## License

alac.js is released under the same terms as the original ALAC decoder from Apple, which is the 
[Apache 2](http://www.apache.org/licenses/LICENSE-2.0) license.

## What's new in this modified version

### ALAC.js
*   24bit support (only stereo)
### Aurora.js
*   Use [cors-anywhere](https://github.com/Rob--W/cors-anywhere) proxy to add CORS headers to the request
