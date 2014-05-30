Android-App-Tutorial
====================

#Android Simple App Tutorial

This is a Tutorial for a simple Android App, which sets a Labels Text to a custom typed it Text, on Button click.

- Create an app and open `/res/layout/main.xml`

We need to add three Views:

>- EditText (user input)
>- Button (function)
>- TextView (output)

We can achieve that by doing:

``` xml

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/tv" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
	    android:id="@+id/btn"
	    android:text="Click" />

```
