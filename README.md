# Android RuntimePermission Helper Class

This is the Helper class to ask Permission, will help you to ask new Runtime Permissions introduced in Android M. it will allows you to check them in background and as well ask for a permission in easy way. just need to ADD THIS :)

#Usage

First Paste the RuntimePermission class in your Project.

Extend Your activity from `RuntimePermission` or you can extends in `BaseActivity`
then set permission of which you want to ask.

**// Define Permission**

    public final String mCalenderPermission = Manifest.permission.WRITE_CALENDAR;
  
**// To set permission use:**  `askPermissionFor(permission, "permissionName")`

    askPermissionFor(mCalenderPermission,"Calendar");     
    
**// To Check whether permission is granted or Not use:** `isPermissionGranted()` **if not then ask using:** `requestPermission();`

    if(!isPermissionGranted()){
        requestPermission();      // if not then ask Permission
    }else{
        // do your stuff here..
    }
    

#Easy to Ask Permission

it will automatically handle all things. if user `deny` permission or check `neverAskAgain` it will handle and also show the alert dialogs to allow permission.


