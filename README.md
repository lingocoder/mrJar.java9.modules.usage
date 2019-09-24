# mrJar.java9.modules.usage

## WTF is This?

A complete working project that demonstrates how to use [*the lingocoder mrJar Gradle plugin*](http://bit.ly/mrJar). Using ***mrJar*** makes it easy to compile a project consisting of a set of collaborating, loosely-coupled [*Java 9<sup>+</sup> JPMS modules*](http://bit.ly/SoTmS). Going one step further than other plugins, ***mrJar*** can also package your modules into separate Modular Multi-Release JAR File (*MRJAR*) distributable artifacts. No other Gradle plugin currently exists (*neither from Gradle nor from the community*) that can create Modular MRJAR Files.

The source code in this demonstration project is essentially a fork of @paulbakker's excellent [*gradle-modules-plugin-example*](http://bit.ly/GrdlModPiEg). Changes in this project include modifications to the *`build.gradle`* files to make them applicable to the ***mrJar*** plugin. And I swapped out the JDK's built-in ServiceLoader with one from the Spring Framework. I also replaced the Gradle-deprecated *`compile`* and *`runtime`* configurations in the original *`build.gradle`* files, with their Gradle-recommended *`api`* and *`implementation`* counterparts. Aside from those sorts of minor implementation details, the functionality in this demo is identical to the original on which it's based.

## What Will I Learn From this Demo?
The most important take away from this *mrJar.java9.modules.usage* demo, is how easy ***mrJar*** makes it to compile and package Java 9<sup>+</sup> modular MRJAR Files. This project also demonstrates that the ***mrJar*** Gradle plugin could serve as a drop-in replacement for the [*gradle-modules-plugin*](http://bit.ly/GrdlModPi)<sup><sup>*1*</sup></sup>. 

## How Do I Run the Demo?

1. Clone or download the project <br />
   • *`cd`* into where you cloned/unzipped the project
2. In a command line terminal, enter: *`./gradlew check`* <br />
   • on Windows: *`gradlew.bat check`*
3. Expected result: <br />
    ```
    ...
    BUILD SUCCESSFUL in 36s
    22 actionable tasks: 22 executed

    ```   
4. Additionally, you can run the *`greeter.runner`* project with:
    ```
    gradlew greeter.runner:run
    
    [system.out] 
    [system.out] Hello and welcome!
    [org.gradle.process.internal.DefaultExecHandle] Changing state to: SUCCEEDED
    ```

## Where Can I Find Out More?

Check out [*the **mrJar** project site*](http://bit.ly/mrjarsite). You'll find more detailed usage instructions listed there. Additionally, I introduced the very first v0.0.1 release of ***mrJar*** to the Gradle Community in [*this Gradle Forums post*](http://bit.ly/mrJarNtro). On top of usage tips for ***mrJar***, that post also has some valuable discussions of Java 9<sup>+</sup> Modules in general. Plus knowledge shared from several others in the community. If you have questions or suggestions, that is one way to reach out. I might post more ***mrJar*** plugin version updates there.

<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />
<br />  
  
  
  
  
  
  
  
  
  
  
______
<sup><sup><sup><sup>*1*</sup></sup></sup></sup><sup>*The **mrJar** Gradle plugin itself, is not derived from any other existing plugin. The **mrJar** plugin is an original software design implementated from scratch.*</sup>

