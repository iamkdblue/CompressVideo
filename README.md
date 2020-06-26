# CompressVideo
A High-performance video compressor for Android using Hardware decoding and encoding API(MediaCodec).

# Motivation
I tried many Video compressor as expected some are not working and outdated ,some are working but not maintaing video resolutions

## Demo
![Demo](/pic/demo.gif)

## Usage
### Call compressVideoLow, compressVideoMedium and compressVideoHigh that indicates 3 quality of compressing.
        VideoCompress.compressVideoLow(String srcPath, String destPath, new VideoCompress.CompressListener() {
            @Override
            public void onStart() {
                //Start Compress
            }

            @Override
            public void onSuccess(String compressVideoPath) {
                //Finish successfully
            }

            @Override
            public void onFail() {
                //Failed
            }

            @Override
            public void onProgress(float percent) {
                //Progress
            }
        });

## Performance

I compress a video which is 2.62MB(00:0:12).

And it took 8 seconds for compressing.

The result of compressing is 479KB.

So it's a great job by MediaCodec :) .

## License
```
MIT License

Copyright (c) 2020 kuldeep Mourya

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
