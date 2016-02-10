# OpenFileDialog
## Synopsis

Show a dialog in your android app that allows the user to select a file or folder from his phones memory or SD card. 

## Screenshots

![alt tag](https://cloud.githubusercontent.com/assets/12089383/12931103/e5adac24-cf30-11e5-9da4-218d86fcdcd5.png)
![alt tag](https://cloud.githubusercontent.com/assets/12089383/12931104/e5c58e7a-cf30-11e5-9ac9-3396f9aad56d.png)
[![ScreenShot](https://cloud.githubusercontent.com/assets/12089383/12931105/e5c7f80e-cf30-11e5-90b3-acc91e859ff5.png)](https://youtu.be/AGe-LnhXk-g)

## Code Example

```java
new OpenFileDialog(context).setOnCloseListener(new OpenFileDialog.OnCloseListener(){
         public void onCancel(){}
         public void onOk(selectedFile){
            Log.i(TAG, "selected file=" + selectedFile);
         }
   })
   .show();
 ```

## Installation

###1. Gracle dependency (JCenter)
Add the following to your build.gradle:
```gradle
compile 'com.github.sebdomdev:open-file-dialog:1.0.1'
```
###2. Maven dependency (JCenter)
Add the following to your pom.xml:
```maven
<dependency> <groupId>com.github.sebdomdev</groupId> <artifactId>open-file-dialog</artifactId> <version>1.0.1</version> <type>pom</type> </dependency>
```

## Optional Settings

```java
OpenFileDialog openFileDialog = new OpenFileDialog(context);
openFileDialog
   //Set the icon that indicates a file in the dialog's list of entries in form of a Resource id.
   .setFileIcon(R.drawable.my_file_icon)
   //Set the icon that indicates a folder in the dialog's list of entries in form of a Resource id.
   .setFolderIcon(R.drawable.my_folder_icon)
   //Set the icon that indicates the up-navigation (i.e. one hierarchy up in the folder-hierarchy) in the dialog's list of entries in form of a Resource id.
   .setFolderUpIcon(R.drawable.my_up_icon)
   //Set if folders can be selected. If the argument is true, folders can be selected instead of files in the dialog.
   .setFolderSelectable(true)
   //Set the text color used for selected files. This should be a color value not a resource id.
   .setFileSelectedColor(R.color.my_file_selected_color)
   //Set the background color used for selected files. This should be a color value not a resource id.
   .setFileSelectedBackgroundColor(R.color.my_file_selected_background_color)
   //Set the text that will be displayed as the title of the dialog.
   .setTitle("Select a file")
   .setTitle(R.string.openfiledialog_title)
```

## MIT License

Copyright (c) 2016 Sebastian Dombrowski

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
