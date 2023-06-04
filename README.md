# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “GalleryControl”.
Developed by:Golla Navya
Registeration Number :212221040048
*/
```
## activity_main.xml:
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
 xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity" android:orientation="vertical">
 <ImageView
           android:id="@+id/imageView"
           android:layout_width="fill_parent"
           android:layout_height="200dp"
           android:scaleType="fitXY" />
 <!-- By using android:spacing we can give spacing between images
 android:animationDuration="3000" -> for animation running -->
 <Gallery
           android:id="@+id/languagesGallery"
           android:layout_width="match_parent"
           android:layout_height="wrap_content"
           android:layout_marginTop="100dp"
           android:animationDuration="2000"
           android:padding="10dp"
           android:spacing="5dp"
           android:unselectedAlpha="50" />
</LinearLayout>
```
## MainActivity.java:
```
MainActivity.java:
package com.example.ga;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Gallery;
import android.view.View;
import android.widget.AdapterView;
import android.widget.Gallery;
import android.widget.ImageView;
import android.widget.SpinnerAdapter;
public class MainActivity extends AppCompatActivity {
     Gallery simpleGallery;
     // CustomizedGalleryAdapter is a java/kotlin
      // class which extends BaseAdapter
      // and implement the override methods.
      CustomizedGalleryAdapter customGalleryAdapter;
      ImageView selectedImageView;
      // To show the selected language, we need this
      // array of images, here taken 10 different kind of
      // most popular programming languages
      int[] images = {
                  R.drawable..tm1,
                 R.drawable..tm2,
                 R.drawable.tm3,
                  R.drawable.tm4,
                 R.drawable.tm5,
                 R.drawable.tm6,
 };
 @Override
 protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        // Our layout is activity_main
        // get the reference of Gallery. As we are showing
        // languages it is named as languagesGallery
        // meaningful names will be good for easier understanding
        simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
        // get the reference of ImageView
        selectedImageView = (ImageView) findViewById(R.id.imageView);
        // initialize the adapter
        customGalleryAdapter = new
CustomizedGalleryAdapter(getApplicationContext(), images);
        // set the adapter for gallery
        simpleGallery.setAdapter(customGalleryAdapter);
 
        // Let us do item click of gallery and image can be identified by its
position
        simpleGallery.setOnItemClickListener((parent, view, position, id) ->
{
        // Whichever image is clicked, that is set in the
selectedImageView
        // position will indicate the location of image
        selectedImageView.setImageResource(images[position]);
 });
 }
}

```

## OUTPUT
![WhatsApp Image 2023-06-04 at 12 18 09](https://github.com/gsuryanavya/Gallery-control/assets/133086963/32695bd8-6a29-453e-8696-57d0092429eb)![WhatsApp Image 2023-06-04 at 12 18 26](https://github.com/gsuryanavya/Gallery-control/assets/133086963/7e8b384a-440c-4091-8c3d-ea0b3540bbbd)





## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.

