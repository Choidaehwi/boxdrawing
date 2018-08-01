# Box-drawing Utilities for Labeling Objects Inside your Pictures

Here are some utility python codes that can help you label your pictures. These codes allows you to surround your object with visualized square lables and translate them into the appropriate form for running yolo. Below are simple descriptions of what each python code does.

## Code Descriptions
### 01_main.py
Executes the labeling program. 
> Requires a "class.txt" file that identifies class names in separate lines.
> Requires an "Examples/demo/" directory that stores 3 demo images(Don't know whether random images work).
> Once the program appears on screen, specify the directory for your images and hit "Load". You will see your very first image file in the center.
> Next, select object class and hit "Confirm" for the object you want to label.
> Click to label. Only 2 clicks are required for labeling an object. Just to be safe, it is recommended that you click from the upper-left corner to the lower-right corner.
> Delete inserted labels by selecting and hitting "Delete" to delete a selected label, or click "ClearAll" to delete all labels for a single image.
> Each visualization of label is stored in ".txt" format inside "Labels/{your directory number}/"

### 02_removeEmptyFile.py
Removes redundant images with no label and empty label files.
> Specify the path to your images and label text files in code. Where to fix is self-evident.

### 03_Labels2Formal.py
Converts labels to appropriate form for feeding yolo network.
> Specify the path to your label text files and path to save the converted labels.

### 04_trainTestList.py
Creates a list of train set and test set in separate ".list" files. They are named "train.list" and "test.list"
> Specify the directory where your Label_formal files reside and where your images reside.
> Specify the percentage to make your test set. [0,100] The remainder will become the train set.

### 05_Formal2Labels.py
In case the original label files are lost, use this code to convert your Label_formal files back to the original label files.

### blur.py
Augment your images by adding blur to your images. 
> Specify blur type, kernel size (x,y), and percentage out of 100 that you want to blur your original images.
> Executing this code will not overwrite the original images but rather create new ones with a prefix added to the original title.

### make_list_general.py
Create a shuffled list of all ".jpg" files resident in the current directory.

### rename_general.py
Rename files in current directory by replacing a certain expression to another.
> Modify replace( {src} , {dst} )
