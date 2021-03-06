# JSQSystemSoundPlayer [![Build Status](https://secure.travis-ci.org/jessesquires/JSQSystemSoundPlayer.png)](http://travis-ci.org/jessesquires/JSQSystemSoundPlayer) [![Version Status](https://cocoapod-badges.herokuapp.com/v/JSQSystemSoundPlayer/badge.png)][docsLink]

A fancy Obj-C wrapper for iOS [System Sound Services](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/SystemSoundServicesReference/Reference/reference.html).

This class is a light-weight, drop-in component to play sound effects, or other short sounds in your iOS app. 
To determine your audio needs, see [Best Practices for iOS Audio](https://developer.apple.com/library/ios/DOCUMENTATION/AudioVideo/Conceptual/MultimediaPG/UsingAudio/UsingAudio.html#//apple_ref/doc/uid/TP40009767-CH2-SW10).
Or, read the tl;dr version:

>*When your sole audio need is to play alerts and user-interface sound effects, use Core Audio’s System Sound Services.*
>
>Your sound files must be:
>
>* No longer than 30 seconds in duration
>* In linear PCM or IMA4 (IMA/ADPCM) format
>* Packaged in a `.caf`, `.aif`, or `.wav` file

If this does not fit your needs, then this control is not for you! 
See [AVAudioPlayer](https://developer.apple.com/library/ios/DOCUMENTATION/AVFoundation/Reference/AVAudioPlayerClassReference/Reference/Reference.html), instead.

![JSQSystemSoundPlayer Screenshot][imgLink] 

## Features

* Play sound effects and alert sounds with a single line of code
* "Play" vibration (if available)
* Sweet and efficient memory management
* Caches sounds (`SystemSoundID` objects) and purges on memory warning

## Requirements

* iOS 6.0+ 
* ARC

## Installation

#### From [CocoaPods](http://www.cocoapods.org)

`pod 'JSQSystemSoundPlayer'`

#### From source

* Drag the `JSQSystemSoundPlayer/` folder to your project.

#### Too cool for [ARC](https://developer.apple.com/library/mac/releasenotes/ObjectiveC/RN-TransitioningToARC/Introduction/Introduction.html)?

* Add the `-fobjc-arc` compiler flag to all source files in your project in Target Settings > Build Phases > Compile Sources.

## Getting Started

````
[[JSQSystemSoundPlayer sharedPlayer] playSoundWithName:@"mySoundFile"
                                             extension:kJSQSystemSoundTypeAIF];

````

And that's all! Extension string constants provided for you: `kJSQSystemSoundTypeCAF`, `kJSQSystemSoundTypeAIF`, `kJSQSystemSoundTypeAIFF`, `kJSQSystemSoundTypeWAV`.

Also see the included demo project: `SoundPlayerDemo.xcodeproj`

## Documentation

Documentation is [available here][docsLink] via [CocoaDocs](http://cocoadocs.org). Thanks [@CocoaDocs](https://twitter.com/CocoaDocs)!

## How To Contribute

1. [Find an issue](https://github.com/jessesquires/JSQSystemSoundPlayer/issues?sort=created&state=open) to work on, or create a new one.
2. Fork me.
3. Create a new branch with a sweet fucking name: `git checkout -b issue_<##>_<featureOrFix>`.
4. Do some motherfucking programming
5. Write Unit Tests, if you can
6. Keep your code nice and clean by adhering to Google's [Objective-C Style Guide](http://google-styleguide.googlecode.com/svn/trunk/objcguide.xml) and Apple's [Coding Guidelines for Cocoa](https://developer.apple.com/library/mac/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html).
7. Don't break shit, especially `master`.
8. Update the documentation header comments.
9. Update the pod spec and project version numbers, adhering to the [semantic versioning](http://semver.org) specification.
10. Submit a pull request.
11. See step 1.

## Credits

Created by [@jesse_squires](https://twitter.com/jesse_squires), a [programming-motherfucker](http://programming-motherfucker.com).

Many thanks to [the contributors](https://github.com/jessesquires/JSQSystemSoundPlayer/graphs/contributors) of this project.

## [MIT License](http://opensource.org/licenses/MIT)

You are free to use this as you please. **No attribution necessary, but much appreciated.**

Copyright &copy; 2013 Jesse Squires

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[docsLink]:http://cocoadocs.org/docsets/JSQSystemSoundPlayer/1.1.0

[imgLink]:https://raw.github.com/jessesquires/JSQSystemSoundPlayer/master/Screenshots/screenshot.png
