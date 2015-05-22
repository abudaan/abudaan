Last Tuesday Chrome has been updated to version 43, this is the first stable release that has the WebMIDI API built in. Obviously, the WebMIDI API is much faster and more stable than any MIDI plugin that we have seen in the past decade.

Unfortunately, the WebMIDI API is not implemented in Chrome for iOS, nor in any other browser but Chrome. It is not to be expected that other browser vendors will implement the WebMIDI API any time soon.

Fortunately we can use the [Jazz plugin][1] in those browsers, and if you use Chris Wilson's [WebMIDIAPIShim][2] you can write your code against the offical WebMIDI API. This means that your project will run both in browsers that have the WebMIDI API implemented, and in browsers that have the Jazz plugin installed.

The WebMIDIAPIShim is called a shim and a polyfill interchangeably. Actually it is both a shim and a polyfill; it is a shim because it intercepts the API calls to the Jazz plugin and converts them to WebMIDI API calls, and it is a polyfill because it adds modern functionality to 'legacy' browsers. See also this [article][3] on Stackoverflow.


 [1]: http://jazz-soft.net/
 [2]: https://github.com/cwilso/WebMIDIAPIShim
 [3]: http://stackoverflow.com/questions/6599815/what-is-the-difference-between-a-shim-and-a-polyfill