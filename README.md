# 360FloatWindowDemo
This Demo shows how to create a float window like 360, and it is form GuoLin's blog, you can see the site: http://blog.csdn.net/guolin_blog/article/details/8689140
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
1. when you donot need a GUI, you can use Service. In this application, we use 

    Intent intent = new Intent(MainActivity.this, FloatWindowService.class);
    startService(intent);
    
to start a new Service;

2. The onStartCommand() function is called by the system every time a client explicitly starts the service.

3. Use the getSystemService(Context.ACTIVITY_SREVICE) function to get ActivityManager object

    ActivityManager mActivityManager = (ActivityManager) getSystemService(Context.ACTIVITY_SERVICE);
    
4. ActivityManager::getRunningTasks(int maxNum) can get a list of the tasks that are currently running.

5. PackageManager::queryIntentActivities(Intent intent, int flags) can retrieve all activies that can be performed for the given intent.

6. When a class just needs to supply some functions, you can modify all the functions in the class with static keyword.

7. Use context.getSystemService(Context.WINDOW_SERVICE) to get the WindowManager.

8. Use WindowManager.addView(View view, ViewGroup.LayoutParams params) to add a view to the window.
