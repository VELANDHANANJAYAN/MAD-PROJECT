## activity_main.xml:
~~~
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <EditText
        android:id="@+id/editTextUsername"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentStart="true"
        android:layout_alignParentTop="true"
        android:layout_alignParentEnd="true"
        android:layout_marginStart="11dp"
        android:layout_marginTop="154dp"
        android:layout_marginEnd="21dp"
        android:hint="Username"
        android:inputType="text" />

    <EditText
        android:id="@+id/editTextPassword"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/editTextUsername"
        android:layout_marginStart="16dp"
        android:layout_marginTop="38dp"
        android:layout_marginEnd="16dp"
        android:hint="Password"
        android:inputType="textPassword" />

    <Button
        android:id="@+id/buttonLogin"
        android:layout_width="135dp"
        android:layout_height="69dp"
        android:layout_below="@id/editTextPassword"
        android:layout_alignParentStart="true"
        android:layout_alignParentEnd="true"
        android:layout_alignParentBottom="true"
        android:layout_marginStart="137dp"
        android:layout_marginTop="150dp"
        android:layout_marginEnd="138dp"
        android:layout_marginBottom="229dp"
        android:text="Login" />

</RelativeLayout>
~~~

## MainActivity.java:
~~~
package com.example.loginscreen;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText editTextUsername, editTextPassword;
    Button buttonLogin;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editTextUsername = findViewById(R.id.editTextUsername);
        editTextPassword = findViewById(R.id.editTextPassword);
        buttonLogin = findViewById(R.id.buttonLogin);

        buttonLogin.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String username = editTextUsername.getText().toString();
                String password = editTextPassword.getText().toString();
                if (username.equals("Velan") && password.equals("saveetha")) {
                    // If login successful, display Hello, World!
                    Toast.makeText(MainActivity.this, "welcome", Toast.LENGTH_SHORT).show();
                } else {
                    // If login failed, display an error message
                    Toast.makeText(MainActivity.this, "Invalid username or password", Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}

~~~

## output:

![Screenshot 2024-05-12 235626](https://github.com/VELANDHANANJAYAN/MAD-PROJECT/assets/119405038/fd8fbf20-5413-4193-8819-040abd681660)

![Screenshot 2024-05-12 235709](https://github.com/VELANDHANANJAYAN/MAD-PROJECT/assets/119405038/af7c47e5-69fd-4028-accc-d7505e47c7b9)


