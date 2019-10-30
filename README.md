### Template for robocode gradle java project

## Instructions

to got it working:
* change robotClassEnemy to your robot's className in gradle.properties
* change robocodeDir to your robocode directory in gradle.properties
* create properties file in src/main/resources just like mine com/kortov/MyRobot.properties
(package structure is neccessary) and remove mine properties
(I'll improve my script later to get rid of this step)
* replace robot.classname in your property file to your className
* (optional) replace robotClassEnemy in gradle.properties to you bot enemy classes (you can specify them with comma)

That's it!

## Gradle tasks usage

# cleanup
invokes clean and removes your files of bot's jar, bots game scenario and imported bots table from your robocode installation directory

# install
builds jar, moves jar and bots game scenario to robocode dir

# start
starts robocode app with your bot game scenario

# superstart
invokes cleanup, install, start tasks sequentially