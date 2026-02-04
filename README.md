# voc2yolo-converter
Converting VOC object detection label format to yolov11 format (hopefuly)

## What my heart and brain said about this repo
So honestly I thought this will be a cool thing to do because maybe my repo can or will help people who want to train an object detection model using YOLO but have the same problem with me.
Yep, the label format is in VOC type (or xaml idk man I don't know every label format for machine learning) and then I checking up github `oh there are alreay a good folks who did it!` knowing that after creating this repo make my will to start and finish this repo recessed.
After that I re-checking my downloaded dataset and stupidly enough I don't realize that the .txt label format is a YOLO labelling format and after that my motivation to even start this repo almost gone.
But then I remember one time I told my-self (gaslight) `You don't deserve anything if you are going to be a quitter all your life pussy ass idiot loser cuck, fucking kill yourself already bro, you piece of idiot shit.` something like that and after that I myself hatred inside me ignited (it always ignited, but like Iman sometimes it burn strong, sometimes it almost died and in that dying state small thing will be enough to make it burn strong again (I'm talking about my self-hate btw, nothing on this about Iman.))
So yep! I'm here starting this repo, hopefully I finish it. Idk man, I hate myself.

## What is inside the label?
So the dataset that I use is this [link to dataset or something](https://www.kaggle.com/datasets/mugheesahmad/sh17-dataset-for-ppe-detection), I want to experiment thing with PPE Safety detection and found this dataset.

### Here is the sample of the VOC label
```xml
<?xml version="1.0" ?>
<annotation>
	<filename>building-construction-building-site-constructing.jpg</filename>
	<size>
		<width>5760</width>
		<height>3840</height>
		<depth>3</depth>
	</size>
	<object>
		<name>gloves</name>
		<pose>Unspecified</pose>
		<truncated>0</truncated>
		<difficult>0</difficult>
		<bndbox>
			<xmin>627</xmin>
			<xmax>1902</xmax>
			<ymin>546</ymin>
			<ymax>2063</ymax>
		</bndbox>
	</object>
</annotation>
```

### Here is the sample of the YOLO .txt label
```
9 0.3875 0.54140625 0.209375 0.3578125
9 0.58046875 0.4390625 0.20625 0.34375
```

### And here is what is inside the data.yaml for YOLO object detection (ultralytics)
```yaml
path: /kaggle/working
train: train_files.txt
val: val_files.txt
test:  test_files.txt

# Classes
names:
  0:  person
  1:  boots
  2:  ear-protection
  3:  safety-glasses
  4:  glove
  5:  helmet
  6:  mask
  7:  medical-suit
  8:  safety-suit
  9:  safety-vest
```

## So what the step I will do?
Yeah I think it's pretty clear that this thing supposed to be an easy one, right? I can use it without help from gpt or something and learn to code properly so I will have less self-hate and impostor syndrom by creating this easy bullish repo, right? `(when I realize this and write, the urge to stick  gunpoint at my mouth roof and making sure it will hit my brain and died is so strong. Because how the fuck I still doing a child-like repo like, WHAT THE FUUUUUUUUUUUUUUCK)`.

By the way this is what I plan to do:

1. Create a function to list all files inside a folder
2. Create a function to open the .xml file (honestly I am not familiar with .xml)
3. Create a function to extract information from .xml file
    - Oh, because I need to store the class in .yaml, I will create a function to extract the object name from the .xml file maybe I will store it inside a json then I will create the .yaml oh, for the number and class name there is two approach, the approach that I give in data.yaml above and this one:

    ```yaml
    names: ['Boots', 'Ear-protection', 'Glass', 'Glove', 'Helmet', 'Mask', 'Person', 'Vest']
    ```
    - If I'm using that approach I think it will be easier? actually it's the same, I'm thinking about changing your position of your label you know, like maybe you want mask = 0 or something, yeah I overthink it again (everytime)
4. Create a main function to repeat the function for every file inside the chosen folder, like you know "easy" (oh my god, my self-hate).
    - Maybe I can do some args so it can be used in terminal

So that's the main quest! What is the side-quests so this shit isn't that shitty?
1. Well I can create a GUI for it, if I finish it with the args, making GUI for it will be much more easier (I guess?) I will use pyqt or tkinter or streamlit, I don't know it's just a sidequest, don't overthink it.
2. I can create micro-feature to some kind of verify or check if the image that referred from the label name are actually "there".
3. I also can create a micro-feature to change the order of the label (yeah what ever)
4. Well if I can make a voc2yolo label converter I supposed to be able to make a yolo2voc label converter, right? The thing is I think it's  doable but I need to remember that it was just a side-quest, it doens't need to be done haha.
5. Oh, yeah, I can make a label deleter, like if you got a database, maybe you don't want every label to be trained, so that feature will be good