# <b>HumanML3D: 3D Human Motion-Language Dataset</b>
<!-- ![tesear_image](./HumanML3D/dataset_showcase.png) -->

HumanML3D is a 3D human motion-language dataset that originates from a combination of [HumanAct12](https://github.com/EricGuo5513/action-to-motion) and [Amass](https://github.com/EricGuo5513/action-to-motion) dataset. It covers a broad range of human actions such as daily activities (e.g., 'walking', 'jumping'), sports (e.g., 'swimming', 'playing golf'), acrobatics (e.g., 'cartwheel') and artistry (e.g., 'dancing'). 

<div  align="center">    
  <img src="./HumanML3D/dataset_showcase.png"  height = "500" alt="teaser_image" align=center />
</div>

### Statistics
Each motion clip in HumanML3D comes with 3-4 single sentence descriptions annotated on Amazon Mechanical Turk. Motions are downsampled into 20 fps, with each clip lasting from 2 to 10 seconds. 

Overall, HumanML3D dataset consists of **14,616** motions and **44,970** descriptions composed by **5,371** distinct words. The total length of motions amounts to **28.59** hours. The average motion length is **7.1** seconds, while average description length is **12** words.

### Data augmentation

We double the size of HumanML3D dataset by mirroring all motions and properly replacing certain keywords in the descriptions (e.g., 'left'->'right', 'clockwise'->'counterclockwise'). 

### KIT-ML Dataset

[KIT Motion-Language Dataset](https://motion-annotation.humanoids.kit.edu/dataset/) (KIT-ML) is also a related dataset that contains 3,911 motions and 6,278 descriptions. We processed KIT-ML dataset following the same procedures of HumanML3D dataset, and provide the access in this repository. However, if you would like to use KIT-ML dataset, please remember to cite the original paper.

## Download Data
An example is provided in this repository (./HumanML3D).

Download [HumanML3D](https://drive.google.com/drive/folders/1e437ofkMW_C6KnP2ef7JY_UuX7XN9_zZ?usp=sharing) dataset.

Download [KIT-ML](https://drive.google.com/drive/folders/1MnixfyGfujSP-4t8w_2QvjtTVpEKr97t?usp=sharing) dataset.

### Data Structure
```sh
<DATA-DIR>
./animations.rar        //Animations of all motion clips in mp4 format.
./new_joint_vecs.rar    //Extracted rotation invariant feature and rotation features vectors from 3d motion positions.
./new_joints.rar        //3d motion positions.
./texts.rar             //Descriptions of motion data.
./Mean.npy              //Mean for all data in new_joint_vecs
./Std.npy               //Standard deviation for all data in new_joint_vecs
./all.txt               //List of names of all data
./train.txt             //List of names of training data
./test.txt              //List of names of testing data
./train_val.txt         //List of names of training and validation data
./val.txt               //List of names of validation data
```
HumanML3D data follows the SMPL skeleton structure with 22 joints. KIT-MLh have 21 skeletal joints. Refer to paraUtils for detailed kinematic chains.

The file named in "MXXXXXX.\*" (e.g., 'M000000.npy') is mirrored from file with correspinding name "XXXXXX.\*" (e.g., '000000.npy'). Text files and motion files follow the same naming protocols, meaning texts in "./texts/XXXXXX.txt"(e.g., '000000.txt') exactly describe the human motions in "./new_joints(or new_joint_vecs)/XXXXXX.npy" (e.g., '000000.npy')



## Installation

## Process Data


## Animate Data
