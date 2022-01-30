# ImageCaptionGeneratorDeployment
Files used for the deployment of an image caption generator for CS554/master's essay.

To use the model, follow these instructions.
Clone the repository and nagivate to the directory it was installed to.
Run the command "pip install -r requirments.txt" to install all the necessary dependencies.
Next unzip the checkpoints.zip file.
Then run the command "python caption_app <image_url>", where <image_url> is the actual
url of the image you want the model to generate a caption for. 
The model should then process the image and output a caption for it. Keep in mind that
this model requires a gpu to work, so it may not run on your local machine if you do not
have a gpu. In this case you could either access the model using the link in the next
paragraph, or try transitioning the code in caption_app to a notebook in google colab.

Our model is also deployed online, so if you would like to use it without cloning the repo,
you can just paste the following link in a browser,
http://jinchispace.com:5001/?image_url=<image_url>
once again, replacing <image_url> with the actual url of an image.

Here I will give a brief rundown of what each file does.
caption_app.py contains the actual code for out model, while the other three files are
just helpers to assist the functions of caption_app.

checkpoints.zip contain the tensorflow checkpoints of the most recent version of our
model. caption_app uses these checkpoints to load the state of our model, so it does
not have to trained again each time we want to use it.

requirments.txt contains the list of all python libraries needed to run caption_app.

tokenizer.pickle is a file that contains a representation of our tokenizer, and was
created using the python pickle library.

Model created by Kenneth Erickson, Mohit Sagar, and Jinchi Zhang.

