# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1.Start Android Studio and create a new project.

2.Design the first screen (Activity 1) with:

    An EditText to input a number.
    A Button labeled "Factorial".
3.In Activity 1:
    Get the number entered by the user.

4.Create an Explicit Intent to navigate to Activity 2.

5.Put the entered number into the intent using putExtra().

6.Start Activity 2 with this intent.

In Activity 2:

Retrieve the number from the intent using getIntent().getIntExtra().

7.Calculate the factorial of the number using a loop or recursion.

8.Display the factorial result on the screen (e.g., in a TextView).


## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by:DHINESH R
Registeration Number :212223220019
*/
```
activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/explicitButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Explicit Intent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
MainActivity.java
```
package com.example.explicitintentdemo; // Replace with your package name

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button explicitButton = findViewById(R.id.explicitButton);

        explicitButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Create an explicit intent to open SecondActivity
                // The first parameter is the context (current activity)
                // The second parameter is the class of the new activity to start
                Intent explicitIntent = new Intent(MainActivity.this, com.example.explicitintentdemo.SecondActivity.class);

                // Start the new activity
                startActivity(explicitIntent);
            }
        });
    }
}
```
activity_second.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".SecondActivity">

    <TextView
        android:id="@+id/secondActivityTextView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="This is Second Activity"
        android:textSize="24sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
SecondActivity.java
```
package com.example.explicitintentdemo;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;

public class SecondActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
        // Your code here, but for this experiment, this is all you need.
    }
}
```

## OUTPUT
<img width="349" height="599" alt="image" src="https://github.com/user-attachments/assets/329f54a4-acf7-491a-be9f-e137c5a0a172" />




## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


