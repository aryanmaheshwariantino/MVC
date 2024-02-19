# MVC
This is the simple random number generator app based on MVC architecture 


Project Structure

    Manifests folder

    It contain AndroidManifest.xml file which is heart of android project.

    This file contains information about our application such as app metadata, android version,app name, activities, permissions, and much more.

    Java folder

    This folder contain source code java/kotlin.

    Resource folder(res)

    This folder contain all non-code resources such as images, audio, video, menus, styles, strings,etc

        drawable

        contains assets like images etc

        layout:

        Contain all xml layouts

        mipmap:

        Contains file to defined icons

        values

        Contains files like strings, dimensions, colors etc

    Gradle Scripts folder

    Gradle is project management tool which help to manage dependency , build of the projects.

    Gradle folder contains many files used to defined number of configuraion files.

        build.gradle(project)

        Is used to specify global build configurations for the entire project, including the repositories where dependencies can be found and the version of the Android build tools to use.

        build.gradle(module)

        Is used to specify the build configurations for a specific module within the project, such as the dependencies, build tools, and other settings needed to build and run the app.

        gradle.setting

        Is used to specify project-wide settings for the build process, including which modules should be included in the project and how they should be organized.

        gradle-wrapper.properties

        Is used to specify the version of Gradle to use for the build process.

-------------------------------------------------------------------------

Android components -->

Activities -->  collection of multiple screens.
ui in xml and ux in kotlin.

Services --> all the background process that not include user interface, long process h jisme user apni app long open nhi rakhega 
ex. downloading process.


class MyService : Service() {
    override fun onBind(intent: Intent?): IBinder? {
        // Implement onBind if needed
        return null
}


BroadCast Receivers --> it simply respond to broadcast messages from other applications or from the system.

ex: call,messages
truecaller ne broadcast reciever laga rakha h , event recieve krne ke baad vo set of instruction execute krdeta h jo usne onrecive me laga rakhe h.

class MyReceiver : BroadcastReceiver() {
    override fun onReceive(context: Context?, intent: Intent?) {
        // Implement what you want to do when the broadcast is received
    }
}

Content Providers : it supplies data from one application to others on request.

class MyContentProvider : ContentProvider(){
    
    override fun onCreate(): Boolean {
        // Initialize your content provider on creation
        return true
    }
}

------------------------------------------------------------
MVC Architecture : Modal view Controller
ex: restaurant example

Model: The Model represents the data and business logic of the application. 

data classes, database operations, network requests, etc.

View: The View represents the UI (User Interface) elements of the application.

Controller: The Controller acts as an intermediary between the Model and the View.

Model handles data, View displays UI, Controller manages user interactions.
 
---------------------------->

Need of Architecture: to mainly focus on sepration of concerns, unit testing.

In MVP we are using interface bewteen the view and the presentation layer to interact.

In MVVM thers is observables in viewmodel that interact with view to interact with that

