
# MAD-EXP-1-To-Create-a-HelloWorld-Activity-using-all-Lifecycles-Methods-to-Display-Messages
# AIM:
To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

# EQUIPMENTS REQUIRED:
Latest Version Android Studio

# ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

# PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by: S. SAHITHYA
Registration Number : 212221040140
*/
activity_main.xml :

<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</android.support.constraint.ConstraintLayout>
MainActivity.java :

package com.example.exp1;
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast.makeText(this, "onCreate Called", Toast.LENGTH_SHORT).show();
    }

    @Override
    protected void onRestart(){
        Toast.makeText(this, "onRestart Called", Toast.LENGTH_SHORT).show();
        super.onRestart();
    }
    @Override
    protected void onStart(){
        Toast.makeText(this, "onStart Called", Toast.LENGTH_SHORT).show();

        super.onStart();
    }
    @Override
    protected void onResume(){
        Toast.makeText(this, "onResume Called", Toast.LENGTH_SHORT).show();

        super.onResume();
    }
    @Override
    protected void onPause(){
        Toast.makeText(this, "onPause Called", Toast.LENGTH_SHORT).show();

        super.onPause();
    }
    @Override
    protected void onStop(){
        Toast.makeText(this, "onStop Called", Toast.LENGTH_SHORT).show();

        super.onStop();
    }
    @Override
    protected void onDestroy(){
        Toast.makeText(this, "onDestroy Called", Toast.LENGTH_SHORT).show();

        super.onDestroy();
    }
}
```
# OUTPUT:
![image](https://github.com/Sahithya7/Mobile-Application-Development/assets/133002193/e6e9b6d8-a435-4ac1-b5b3-c3a2ad011bcc)
![image](https://github.com/Sahithya7/Mobile-Application-Development/assets/133002193/f1914e3f-1d02-4f8e-9bd9-f4ab718255ac)
![image](https://github.com/Sahithya7/Mobile-Application-Development/assets/133002193/0bf8c4e9-b82a-4b5d-b886-47cbb6c7e24d)
![image](https://github.com/Sahithya7/Mobile-Application-Development/assets/133002193/b5cf80b5-c63a-48f0-a77a-bd67a5d24fe7)
![image](https://github.com/Sahithya7/Mobile-Application-Development/assets/133002193/fd6fea2e-eb73-4ecf-9f26-f15cb87ed016)
![image](https://github.com/Sahithya7/Mobile-Application-Development/assets/133002193/49a42769-9747-4bf9-9b91-3ca8ae3dd3b3)
# RESULT:
Thus, a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
