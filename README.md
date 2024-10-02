# Transcoder-0.9.1-buildsrc

- Due to my use of flutter's vide_compress:3.1.2 (as of 2022.11.21), it references transcoder:0.9.1 

> throws an error: 'Execution failed for task ':app:checkDebugAarMetadata'

- For could not find com.otaliastudios:transcoder:0.9.1.'   I have checked the issue sections for both vide_compress and transcoder, and it is mentioned that the dependency should be available from the jcenter repository (from 2022.11.25 to 2023.8). 
- However, as of 2024.10.02, for some unknown reason, I cannot find the transcoder:0.9.1 dependency in jcenter or any other Maven repositories.
- Therefore, I manually downloaded the source code from the Github repository, buildit, and installed it locally, which then allowed my application to compile successfully. 



- This repository contains the source code that I used for compilation, with only two minor modifications in their respective build.gradle files, mainly commenting out the dependencies and configurations related to bintray (a repository). Here are the binaries I have compiled.



- use: Oracle JDK 1.8.0_391， gradle wrapper
- build cmd：for Transcoder-0.9.1 and Egloo-0.4.0 both are `./gradlew.bat :lib:install`, and invoke this cmd in their respective directories.