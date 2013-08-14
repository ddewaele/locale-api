##Introduction

This is a library project for the [Locale Developer API](http://www.twofortyfouram.com/developer).

##Goal

This is a mavenized version of the Locale library project (that can be downloaded from the [Locale Developer API website](http://www.twofortyfouram.com/developer). 
I've added a valid pom.xml so that project can be easily built using maven.
 
##Maven build

In order to build the project you'll need to set your ```ANDROID_HOME``` environment variable to point to your SDK.

	ANDROID_HOME=C:\SOFT\adt-bundle-windows-x86_64-20130514\sdk

Building the project should result in this:

	[INFO] Scanning for projects...
	[INFO]                                                                         
	[INFO] ------------------------------------------------------------------------
	[INFO] Building locale-api 4.2
	[INFO] ------------------------------------------------------------------------
	[INFO] 
	[INFO] --- android-maven-plugin:3.6.0:generate-sources (default-generate-sources) @ locale-api ---
	[INFO] ANDROID-904-002: Found aidl files: Count = 0
	[INFO] ANDROID-904-002: Found aidl files: Count = 0
	[INFO] Manifest merging disabled. Using project manifest only
	[INFO] C:\SOFT\adt-bundle-windows-x86_64-20130514\sdk\build-tools\android-4.2.2\aapt.exe [package, --non-constant-id, -m, -J, C:\PROJECTS\Android\Locale\display\locale-api\target\generated-sources\r, -M, C:\PROJECTS\Android\Locale\display\locale-api\AndroidManifest.xml, -S, C:\PROJECTS\Android\Locale\display\locale-api\res, --auto-add-overlay, -A, C:\PROJECTS\Android\Locale\display\locale-api\assets, -I, C:\SOFT\adt-bundle-windows-x86_64-20130514\sdk\platforms\android-17\android.jar]
	[INFO] 
	[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ locale-api ---
	[INFO] Using 'UTF-8' encoding to copy filtered resources.
	[INFO] skip non existing resourceDirectory C:\PROJECTS\Android\Locale\display\locale-api\src\main\resources
	[INFO] skip non existing resourceDirectory C:\PROJECTS\Android\Locale\display\locale-api\target\generated-sources\extracted-dependencies\src\main\resources
	[INFO] 
	[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ locale-api ---
	[INFO] Changes detected - recompiling the module!
	[INFO] Compiling 6 source files to C:\PROJECTS\Android\Locale\display\locale-api\target\classes
	[INFO] 
	[INFO] --- android-maven-plugin:3.6.0:proguard (default-proguard) @ locale-api ---
	[INFO] 
	[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ locale-api ---
	[INFO] Using 'UTF-8' encoding to copy filtered resources.
	[INFO] skip non existing resourceDirectory C:\PROJECTS\Android\Locale\display\locale-api\src\test\resources
	[INFO] 
	[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ locale-api ---
	[INFO] No sources to compile
	[INFO] 
	[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ locale-api ---
	[INFO] 
	[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ locale-api ---
	[INFO] Building jar: C:\PROJECTS\Android\Locale\display\locale-api\target\locale-api.jar
	[INFO] 
	[INFO] --- android-maven-plugin:3.6.0:apklib (default-apklib) @ locale-api ---
	[INFO] C:\SOFT\adt-bundle-windows-x86_64-20130514\sdk\build-tools\android-4.2.2\aapt.exe [package, -f, -M, C:\PROJECTS\Android\Locale\display\locale-api\AndroidManifest.xml, -S, C:\PROJECTS\Android\Locale\display\locale-api\res, --auto-add-overlay, -A, C:\PROJECTS\Android\Locale\display\locale-api\assets, -I, C:\SOFT\adt-bundle-windows-x86_64-20130514\sdk\platforms\android-17\android.jar, -F, C:\PROJECTS\Android\Locale\display\locale-api\target\locale-api.ap_]
	[INFO] C:\PROJECTS\Android\Locale\display\locale-api\libs does not exist, looking for libraries in target directory.
	[INFO] Building jar: C:\PROJECTS\Android\Locale\display\locale-api\target\locale-api.apklib
	[INFO] 
	[INFO] --- maven-install-plugin:2.4:install (default-install) @ locale-api ---
	[INFO] Installing C:\PROJECTS\Android\Locale\display\locale-api\target\locale-api.apklib to C:\Users\Davy\.m2\repository\com\twofortyfouram\locale-api\4.2\locale-api-4.2.apklib
	[INFO] Installing C:\PROJECTS\Android\Locale\display\locale-api\pom.xml to C:\Users\Davy\.m2\repository\com\twofortyfouram\locale-api\4.2\locale-api-4.2.pom
	[INFO] ------------------------------------------------------------------------
	[INFO] BUILD SUCCESS
	[INFO] ------------------------------------------------------------------------
	[INFO] Total time: 4.538s
	[INFO] Finished at: Wed Aug 14 12:53:42 CEST 2013
	[INFO] Final Memory: 20M/353M
	[INFO] ------------------------------------------------------------------------

This will result in the Locale API APK Library artifact (apklib) to be put in your local maven repository.
You can then use this library dependency in your own projects like this:

	<dependency>
		<groupId>com.twofortyfouram</groupId>
		<artifactId>locale-api</artifactId>
		<version>4.2</version>
		<type>apklib</type>
	</dependency>	
	 
##Android library projects
For documentation on Android Library Projects, please visit the [Android Developer site](http://developer.android.com/guide/developing/eclipse-adt.html#libraryProject)

