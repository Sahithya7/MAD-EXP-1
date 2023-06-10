# Ex.No: 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as animation and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application


## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: S.SAHITHYA
Registeration Number : 212221040140
*/
```
# Activity_main.xml:
```
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Animation"
    android:id="@+id/textView"
    android:textSize="35dp"
    android:layout_alignParentTop="true"
    android:layout_centerHorizontal="true"
    />

<ImageView
    android:id="@+id/imageView"
    android:layout_width="20dp"
    android:layout_height="100dp"
    android:paddingTop="10dp"
    android:layout_below="@+id/textView"
    android:layout_alignRight="@+id/textView"
    android:layout_alignEnd="@+id/textView"
    android:layout_alignLeft="@+id/textView"
    android:layout_alignStart="@+id/textView"
    app:srcCompat="@android:drawable/btn_star_big_on" />
<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="zoom"
    android:id="@+id/button"
    android:layout_below="@+id/imageView"
    android:layout_alignParentLeft="true"
    android:layout_alignParentStart="true"
    android:layout_marginTop="40dp"
    android:onClick="clockwise"/>

<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="clockwise"
    android:id="@+id/button2"
    android:layout_alignTop="@+id/button"
    android:layout_centerHorizontal="true"
    android:onClick="zoom"/>

<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="fade"
    android:id="@+id/button3"
    android:layout_alignTop="@+id/button2"
    android:layout_alignParentRight="true"
    android:layout_alignParentEnd="true"
    android:onClick="fade"/>

<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="blink"
    android:onClick="blink"
    android:id="@+id/button4"
    android:layout_below="@+id/button"
    android:layout_alignParentLeft="true"
    android:layout_alignParentStart="true" />

<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="move"
    android:onClick="move"
    android:id="@+id/button5"
    android:layout_below="@+id/button2"
    android:layout_alignRight="@+id/button2"
    android:layout_alignEnd="@+id/button2"
    android:layout_alignLeft="@+id/button2"
    android:layout_alignStart="@+id/button2" />

<Button
    android:id="@+id/button6"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_below="@+id/button3"
    android:layout_marginStart="21dp"
    android:layout_marginLeft="21dp"
    android:layout_marginTop="4dp"
    android:layout_toEndOf="@+id/textView"
    android:layout_toRightOf="@+id/textView"
    android:onClick="slide"
    android:text="slide" />
```
# MainActivity.java:
```
package com.example.androidanimation;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.view.animation.Animation;

import android.view.animation.AnimationUtils;

import android.widget.ImageView;

import android.view.View;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
}

public void clockwise(View view){
    ImageView image = (ImageView)findViewById(R.id.imageView);
    Animation animation = AnimationUtils.loadAnimation(getApplicationContext(),
            R.anim.myanimation);
    image.startAnimation(animation);
}

public void zoom(View view){
    ImageView image = (ImageView)findViewById(R.id.imageView);
    Animation animation1 = AnimationUtils.loadAnimation(getApplicationContext(),
            R.anim.clockwise);
    image.startAnimation(animation1);
}

public void fade(View view){
    ImageView image = (ImageView)findViewById(R.id.imageView);
    Animation animation1 =
            AnimationUtils.loadAnimation(getApplicationContext(),
                    R.anim.fade);
    image.startAnimation(animation1);
}

public void blink(View view){
    ImageView image = (ImageView)findViewById(R.id.imageView);
    Animation animation1 =
            AnimationUtils.loadAnimation(getApplicationContext(),
                    R.anim.blink);
    image.startAnimation(animation1);
}

public void move(View view){
    ImageView image = (ImageView)findViewById(R.id.imageView);
    Animation animation1 =
            AnimationUtils.loadAnimation(getApplicationContext(), R.anim.move);
    image.startAnimation(animation1);
}

public void slide(View view){
    ImageView image = (ImageView)findViewById(R.id.imageView);
    Animation animation1 =
            AnimationUtils.loadAnimation(getApplicationContext(), R.anim.slide);
    image.startAnimation(animation1);
}
}
```
# Myanimation.xml:
```
<scale xmlns:android="http://schemas.android.com/apk/res/android"
    android:startOffset="5000"
    android:fromXScale="3.0"
    android:toXScale="0.5"
    android:fromYScale="3.0"
    android:toYScale="0.5"
    android:duration="5000"
    android:pivotX="50%"
    android:pivotY="50%" >
</scale>
Move.xml:
<translate
    android:fromXDelta="0%p"
    android:toXDelta="75%p"
    android:duration="700" />
```
# Fade.xml:
```
<alpha
    android:duration="1000"
    android:fromAlpha="0"
    android:toAlpha="1" />

<alpha
    android:duration="1000"
    android:fromAlpha="1"
    android:startOffset="2000"
    android:toAlpha="0" />
```
# clockwise.xml:
```
<rotate xmlns:android="http://schemas.android.com/apk/res/android"
   android:fromDegrees="0"
   android:toDegrees="360"
   android:pivotX="50%"
   android:pivotY="50%"
   android:duration="5000" >
</rotate>

<rotate xmlns:android="http://schemas.android.com/apk/res/android"
   android:startOffset="5000"
   android:fromDegrees="360"
   android:toDegrees="0"
   android:pivotX="50%"
   android:pivotY="50%"
   android:duration="5000" >
</rotate>
```
# Zoom.xml:
```
<scale
    android:duration="500"
    android:fromXScale="1.0"
    android:fromYScale="1.0"
    android:interpolator="@android:anim/linear_interpolator"
    android:toXScale="1.0"
    android:toYScale="0.0" />
```
# Slide.xml:
```
<scale
    android:duration="500"
    android:fromXScale="1.0"
    android:fromYScale="1.0"
    android:interpolator="@android:anim/linear_interpolator"
    android:toXScale="1.0"
    android:toYScale="0.0" />
```
## OUTPUT
![image](https://github.com/Sahithya7/Moblie-Application-Development/assets/133002193/eaeae451-fb2a-4316-933e-a2330e703e9f)



![image](https://github.com/Sahithya7/Moblie-Application-Development/assets/133002193/285aa997-42d5-48b4-bb36-71831e282a1c)



![image](https://github.com/Sahithya7/Moblie-Application-Development/assets/133002193/927e67e1-1fbf-4c74-96e5-09996a125be0)



## RESULT
Thus, to develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio has been executed successfully.
