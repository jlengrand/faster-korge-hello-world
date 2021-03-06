# A (faster) fork from the [korge-hello-world](https://github.com/korlibs/korge-hello-world)?

_EDIT : Seems like it was a temporary issue, and I could not reproduce it any more a couple hours later. Maybe something related to the Maven servers? Ignore the content of that repository_.

I just started playing around with the (awesome) [Korge](https://korge.org/) Kotlin Game Engine.

One of the things that really disturbed is that when creating a new Hello World project, the compilation only would take almost **2 minutes** before the game could run.
After some investigations, it looks like all the time is spent in the [`KorgeGradlePlugin`](https://github.com/korlibs/korge-plugins/tree/master/korge-gradle-plugin) (but I am too novice to know why at the moment). 

Check the result of the scan [here](https://scans.gradle.com/s/bbiqxktq3dhvu).

Thanks to the great help from [LeHaine](https://github.com/LeHaine), I could reduce this drastically.
The numbers below are only for reference, but you can try it yourself.

|Project | Command | Machine| Average time |
--- | --- | --- | ---
|[Korge project hello world](https://github.com/korlibs/korge-hello-world)|`./gradlew runJvm`|MBP 2017|~1m50s|
|[Korge project hello world](https://github.com/korlibs/korge-hello-world)|`./gradlew runJvm`|Win 10 i7 16Gb|~1m20s|
|[Faster korge hello world](https://github.com/jlengrand/faster-korge-hello-world)|`./gradlew runJvm`|MBP 2017| ~20s |
|[Faster korge hello world](https://github.com/jlengrand/faster-korge-hello-world)|`./gradlew runJvm`|Win 10 i7 16Gb|~5s|

Thanks again to [LeHaine](https://github.com/LeHaine) (and others on the Discord).

_Note: I am pretty sure that this performance gain comes at a cost. If someone knows enough to tell me what it can be, I'm all ears. For the moment, I'll take the large performance gain to increase my feedback loop speed_.
