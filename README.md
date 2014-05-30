Android-App-Tutorial
=================

#Android Simple App Tutorial

This is a Tutorial for a simple Android App, which sets a Labels Text to a custom typed it Text, on Button click.

- Create an app and open `/res/layout/main.xml`

We need to add three Views:

>- EditText (user input)
>- Button (function)
>- TextView (output)

We can achieve that by doing:

``` xml

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/et" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
	    android:id="@+id/btn"
	    android:text="Click" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/tv" />
```

- Now we need to add a function to the Button:

``` xml

    android:onClick="changeText"
```

- We are finished with the Layout (UI) for now, open up `src/.../MainActivity.java`

Now, under:

``` java

    public class MainActivity extends Activity {
```

we can define our Global Variables!

- Add following view declarations:

``` java

    EditText et;
    Button btn;
    TextView tv;
```

Of course we need to tell out App, which view is defined in which variable.

- In `onCreate`, which is called once the App is started, add following declaration:

``` java

    et = (EditText)findViewById(R.id.et);
    btn = (Button)findViewById(R.id.btn);
    tv = (TextView)findViewById(R.id.tv);
```

Note that `R.id.et/btn/tv` is the id name from your `main.xml`!

- Finally we can add functionality to our Button/App!

Create a function for your button, named the same as your `onClick` attribute in the `main.xml`:

``` java

    public void changeText(View view) {

    }

```

If you are calling a function via `onClick`, don't forget to add the `(View view)`, or else your App will crash!

- Make the Button print our Input:

To make our Button print our input we need to know about two methods:

>`TextView.setText(string);`

>This sets a TextViews Text to a string like "Hello World!".

and

>`EditText.getText().toString();`

>This reads the input of an EditText, you can save it into a String.

- With this knowledge we can complete our `changeText` function!

``` java

    public void changeText(View view) {
 
        String ourInput = et.getText().toString();
        tv.setText(ourInput);

    }

```

- You now have successfully created a simple Android App!

##Gratulations! ;)
