# A (faster) fork from the [korge-hello-world](https://github.com/korlibs/korge-hello-world)

I just started playing around with the (awesome) [Korge](https://korge.org/) Kotlin Game Engine.

One of the things that really disturbed is that when creating a new Hello World project, the compilation only would take almost 2 minutes before the game could run.
After some investigations, it looks like all the time is spent in the KorgeGradlePlugin (but I am too novice to know why at the moment). Check the result of the scan [here](https://scans.gradle.com/s/bbiqxktq3dhvu).



Thanks to the great help from [LeHaine](https://github.com/LeHaine), I could reduce this drastically.

The numbers below are only for reference, but you can try it yourself.

* Clone the [Korge project hello world])(https://github.com/korlibs/korge-hello-world), and run `./gradlew runJvm`. 
  * On my 2017 MBP and my gaming rig, it takes consistently between 1m20s and 2m30s before the template starts.
* Clone this [project]() , and run `./gradlew runJvm`.
  * On my 2017 MBP and my gaming rig, it takes consistently between **5s and 20s**.
    

Thanks again to [LeHaine](https://github.com/LeHaine) (and others on the Discord).

_Note: I am pretty sure that this performance gain comes at a cost. If someone knows enough to tell me what it can be, I'm all ears. For the moment, I'll take the large performance gain to increase my feedback loop speed_.

Thanks!