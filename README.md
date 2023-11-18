
# Ex.No:2 Develop an application that uses Font Size using Android Studio.


## AIM:
To develop an application that uses Font Size using android studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Create a New Android Project:
              • Click New in the toolbar.
              • In the window that appears, open the Android folder, select Android Application Project,
              and click next.
              • Provide the application name and the project name and then finally give the desired
              package name.
              • Choose a launcher icon for your application and then select Blank Activity and then click
              Next
              • Provide the desired Activity name for your project and then click Finish.

Step 2: Create a New AVD (Android Virtual Device):
        • click Android Virtual Device Manager from the toolbar.
        • In the Android Virtual Device Manager panel, click New.
        • Fill in the details for the AVD. Give it a name, a platform target, an SD card size, and
        a skin (HVGA is default).
        • Click Create AVD and Select the new AVD from the Android Virtual Device
        Manager and click Start.

Step 3: Design the graphical layout with a text view and two command buttons.

Step 4: Run the application.

Step 5:On pressing the change font size button, the size of the font gets altered.       
       
Step 6:Close the Android project. 


## Program:
 ```
/*
Program to Develop an application that uses Font Size using Android Studio .
Developed by: Lathika Sunder
RegisterNumber:212221230054 
*/
```

## MainActivity.java:

~~~
package com.firstapp.fontsize;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.app.Activity;
import android.graphics.Typeface;
import android.graphics.Color;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;


public class MainActivity extends AppCompatActivity {
    float font = 24;
    int i = 1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t1 = (TextView)findViewById(R.id.textView1);
        Button b1 = (Button)findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener()    {
            public void onClick(View view) {
                t1.setTextSize(font);
                font = font+4;
                if(font==40)
                    font = 20;
            }
        });


    }
}

~~~

## activity_main.xml:
~~~
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <TextView
        android:id="@+id/textView1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="70dp"
        android:gravity="left"
        android:text="HELLO WORLD"
        android:textSize="20sp"
        android:textStyle="bold"
        tools:layout_editor_absoluteX="70dp"
        tools:layout_editor_absoluteY="376dp" />

    <Button
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20sp"
        android:gravity="center"
        android:text="Change Font Size"
        tools:layout_editor_absoluteX="40dp"
        tools:layout_editor_absoluteY="456dp" />
    </RelativeLayout>
~~~

## Output:

![233335826-9b2098b4-3c60-450a-99b0-93a270dcfe23](https://user-images.githubusercontent.com/93427201/233931277-65592320-c1e4-4b2b-a89d-9f58029bd02d.png)

![image](https://user-images.githubusercontent.com/93427201/233931663-df175e0d-074f-48a7-ba1a-2c05c0491695.png)

## Result:
Thus, the program for android application, Font Size was executed successfully using Android Studio.
