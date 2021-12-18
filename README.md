demo of the git



public int square(int x, int y) {
    return x * y;
}


git remote add backup https://github.sydney.edu.au/usyd1234/repo1.git

git remote add group  https://github.sydney.edu.au/SOFT2412-2021S2/repo1.git

//commit already been made
git push backup main

git push group main

git pull group main
git push backup main


plugins {
id 'application'
id 'jacoco'
}
repositories {
mavenCentral()
}
dependencies {
testImplementation 'org.junit.jupiter:junit-jupiter:5.7.2'
implementation 'com.google.guava:guava:30.1.1-jre'
}
application {
mainClass = 'project.Program'
}
jacocotestreport{

}
tasks.named('test') {
useJUnitPlatform()
finalizedby jacocotestreport
or 
doLast{
    jacocotestreport
}
}

printText{
    println "pp"
}

build{
    doLast{
        println "build provess is over"
    }
}

gradle tasks --all
//gradle -m build
##some new change
