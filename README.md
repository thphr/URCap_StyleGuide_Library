URCap_StyleGuide_Library


The URCap StyleGuide Library enables an easier implementation of the user interface in the URCap that has the look and feel in accordance with the requirement of UR for e-series. (https://plus.universal-robots.com/download-center/style-guide-e-series/) 

To use this library it is required to have maven installed on the computer. Download the library or clone for new updates.

To add this to the URCap project as a third-party library, follow the bullets points below to add the library:
 
4.a) From the terminal, direct to the "URStyleGuide.jar" and execute following maven command in the terminal: 

	mvn install:install-file -Dfile=URStyleGuide.jar -DgroupId=com.ur -DartifactId=StyleGuide -Dversion=1.0 -Dpackaging=jar
      
4.b) Insert the following in the pom.xml file of the URCap project as part of the \<Import-Package> tag:
      
	com.ur.style*;version="[1.0)"
  
4.c) Insert the following in the pom.xml file below the \<Import-Package> tag:
     	
	<Embed-Dependency>StyleGuide;scope=compile|runtime</Embed-Dependency>
  
4.d) Insert the following as a part of the \<dependencies> tag:
     	
	<dependency>
        	<groupId>com.ur</groupId>
		<artifactId>StyleGuide</artifactId>
        	<version>1.0</version>
	</dependency>

For an example on how the library is implemented in a URCap, please refer to the following github link:
https://github.com/thphr/URStyleGuideExample

Link direct to the class that implements the URStyleGuide Library: 
https://github.com/thphr/URStyleGuideExample/blob/main/com.thph.StyleGuideExample/src/main/java/com/thph/StyleGuideExample/impl/ExampleProgramNodeView.java
