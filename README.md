# Android-errors-and-solutions-

------------------------------------------------------------------------------------------------------------------------------------------
Error 1 -> 

      # Gradle sync failed with Android Studio 3.1: Uninitialized object exists on backward branch 70
      
      It's resolved my issue when I used embedded JDK(recommended) option

      Do this:

      Project Structure -> SDK Location -> Select "Use embedded JDK(recommended)"
      
      link - > https://stackoverflow.com/questions/49515100/gradle-sync-failed-with-android-studio-3-1-uninitialized-object-exists-on-backw#comment86058048_49518396
------------------------------------------------------------------------------------------------------------------------------------------

Error 2 ->

      #Failed to load AppCompat ActionBar with unknown error in android studio  Render problem for layouts
      
      change the style.xml 
      
      <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
      </style>
      
      to:

      <style name="AppTheme" parent="Base.Theme.AppCompat.Light.DarkActionBar">
      </style>
      
------------------------------------------------------------------------------------------------------------------------------------------   

Error 3 -> 

      # Namespace 'app' is not bound
      Just add xmlns:app="http://schemas.android.com/apk/res-auto" in the menu item property
      or alt+enter add quickly. 
      
      
------------------------------------------------------------------------------------------------------------------------------------------   

Error 4 ->

      # Permission is only granted to system app 
      # Issue id : ProtectedPermissions
    
      # https://stackoverflow.com/questions/38072616/permission-required-to-use-usagestatsmanager
      
      # <manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">
    
      # add xmlns:tools="http://schemas.android.com/tools" into manifest tag

------------------------------------------------------------------------------------------------------------------------------------------  

Error 5 ->

      # Failed to finalize session : INSTALL_FAILED_SHARED_USER_INCOMPATIBLE: Package couldn't be installed in 
      has no signatures that match those in shared user android.uid.system; ignoring!
      
      # Change the  android:sharedUserId="" in manifest file.
      
------------------------------------------------------------------------------------------------------------------------------------------       

Error 6 -> 

      # attribute ':menu' not found. or attribute ':headerLayout' not found. 
      
      # add to build.gradle file dependencies 
      # implementation 'com.android.support:design:28.0.0'   
      # <28.0.0> version should be same appcompat version
      
------------------------------------------------------------------------------------------------------------------------------------------       
