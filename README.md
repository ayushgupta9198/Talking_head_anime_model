**Code for the Talking Head Anime from a Single Image.
**

**Hardware Requirements**

This piece of code requires a recent and powerful Nvidia GPU to run. I have personally run the code on a Geforce GTX 730 and also it will run on CPU version as well but the performance may vary.

Also, the peppeteer tool requires a webcam but also i have modified the code into both the options either you can run the code with webcam or passing with Video.

**Dependencies : **
Python >= 3.6
pytorch >= 1.4.0
dlib >= 19.19
opencv-python >= 4.1.0.30
pillow >= 7.0.0
numpy >= 1.17.l2

If you install these packages, you should be all good.

**Prepare the Data
**
After you cloned this repository to your machine's storage, you need to download the models:

Download the main models from this link. Unzip the file into the data directory under the project's root. The models are released separately with the Creative Commons Attribution 4.0 International License.

Download shape_predictor_68_face_landmarks.dat and save it to the data directory. You can download the bzip archive from here. Do not forget to uncompress.

To play with the demo, you can use the 5 images I included in the data/illust. Or, you can prepare some character images by yourself. Images that can be animated must satisfy the following requirements:

It must be in PNG format.
It must be of size 256 x 256.
The head of the character must be contained in the center 128 x 128 box.
It must have 4 channels (RGBA).
Pixels that do not belong to the character's body must have value (0,0,0,0). In other words, the background must be transparent.

**Running the Program**

Change directory to the root directory of the project. To run the manual poser, issue the following command in your shell:

python app/manual_poser.py

**To run the puppeteer, issue the following command in your shell:**

python app/puppeteer.py
