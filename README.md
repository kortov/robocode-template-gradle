# Template for robocode gradle java project

## Instructions

to got it working:
* install jdk 8, 11 or later [Oracle JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html), [Liberica JDK](https://bell-sw.com/)
* install [robocode](https://robocode.sourceforge.io/) on your computer 
* change `robotClass` to your robot's `className` in `gradle.properties`
* change `robocodeDir` to your robocode installation directory in `gradle.properties`
* create properties file with your class name in `src/main/resources` just like mine `com/kortov/MyRobot.properties`
(package structure is neccessary) and remove my properties
(I'll improve my script later to get rid of this step)
* replace `robot.classname` and `robot.version` in your resources properties file to your `robotClass` and `robotVersion` values from gradle.properties
(I'll improve it later) 
* (optional) replace `robotClassEnemy` in gradle.properties to your downloaded or built bot enemy classes (you can specify them with comma). Bots classes or jars should exist in robocodeDir/robots
* cd in console to a project folder and run `gradlew superstart` in console (`./gradlew superstart` on linux)

That's it! Your bot will be in `projectDirectory/build/libs` and in `robocodeDir/robots`

### Change version of the bot
Manually change versions in two properties from `src/main/resources` and `gradle.properties` otherwise robocode will play the old version or won't find the new one

## Gradle tasks usage

### cleanup
invokes clean and removes your files of bot's jar, bots game scenario and imported bots table from your robocode installation directory

### install
builds jar, moves jar and bots game scenario to robocode dir

### start
starts robocode app with your bot game scenario

### superstart
invokes cleanup, install, start tasks sequentially
