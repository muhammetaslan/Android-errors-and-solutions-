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
