####RTL-TextJustify-Android is an extension of project hosted here [TextJustify-Android](https://github.com/bluejamesbond/TextJustify-Android). As [TextJustify-Android](https://github.com/bluejamesbond/TextJustify-Android) doesn't seem to support RTL scripts like Urdu, Persian, Arabic etc., this projcet is aimed to support these languages.


![Logo](https://raw.github.com/bluejamesbond/TextJustify-Android/master/__misc/textjustify%20design%20logo%20%5Ba%5D.png)
=======
**Simple Android Full Justification**
Overview
=======
This is very simple. What you want to do is get the library itself and add it to your Android project.

Setup
=======
Looks very accurate and neat. Small issues may arise but can be easily sorted out if users post their issues on Github. To use it, all you have to do is include the `TextViewEx.java` and `TextJustifyUtils.java` in your project. Then you may use as you would the built-in  `TextView`. 

To improve performance on large TextViews, you must enable optimization. To do so, you must use `setDrawingCacheEnabled(bool)`. Using this increases speed, but it also requires more memory.

```xml

<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context=".MainActivity" >
    
    <com.textjustify.TextViewEx
        android:id="@+id/textview"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />
        
</ScrollView>

```
```java

@Override
protected void onCreate(Bundle savedInstanceState) 
{
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main); 
    
    TextViewEx txtViewEx = (TextViewEx) findViewById(R.id.textViewEx);
    txtViewEx.setText("Insert your content here", true); // true: enables justification
    
    // Optional hyphenation:
    // Words syllables must be pre-separated with a syllableSeparator string (character)
    // Example: A com*put*er is a gen*er*al pur*pose de*vice that...
    txtViewEx.setHyphenate(true, "*");
}

```
Result
=======
**Comparison**

![Logo](http://i.imgur.com/xbzYStc.png)


Notes
=======
HTML formatting will cause you to have expected results.

Contributors
=======

```js
bluejamesbond
fscz
shayanpourvatan
Saleh-Hassan
```
