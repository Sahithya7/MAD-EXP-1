# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:S.Sahithya
Registeration Number :212221040140
*/
```
# Activity_xml File:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginStart="4dp"
    android:layout_marginTop="52dp"
    android:text="@string/enter_an_url"
    android:textSize="26sp"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    tools:ignore="ExtraText" />

<EditText
    android:id="@+id/E1"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="120dp"
    android:ems="10"
    android:inputType="textPersonName"
    android:text=""
    android:textColor="#2196F3"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.791"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/button"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginBottom="484dp"
    android:text="Jump Into"
    app:backgroundTint="#4CAF50"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.462"
    app:layout_constraintStart_toStartOf="parent" />


</androidx.constraintlayout.widget.ConstraintLayout>
```
# MainActivity.java File:
```
package com.example.intent_implementation;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
Button button;
EditText e1;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    button = findViewById(R.id.button);
    e1 = findViewById(R.id.E1);
    button.setOnClickListener(view -> {
        String url = e1.getText().toString();
        Intent i1 = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
        startActivity(i1);
    });
}
}
```
## OUTPUT
![image](https://github.com/Sahithya7/Moblie-Application-Development/assets/133002193/097e667a-e43f-4a1f-8aaa-37cb4c7af01c)

![image](https://github.com/Sahithya7/Moblie-Application-Development/assets/133002193/40d7efd4-6985-454b-b6f7-4b55718d870c)


![image](https://github.com/Sahithya7/Moblie-Application-Development/assets/133002193/92bb90f4-8605-4c8e-9a55-a87e0fec9ee1)


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


