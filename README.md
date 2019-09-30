# CreepyFaces Tutorial

Welcome to the CreepyFaces Tutorial!

In this tutorial, we will teach you how to create Creepy Faces like this one:

<table border="0"><tr><td>
<img src="https://raw.githubusercontent.com/shwars/FaceArt/master/notebooks/img/PhoBoGuy.png"/>
</td><td>
<img src="https://raw.githubusercontent.com/shwars/FaceArt/master/notebooks/img/PhoBoGuy1.png"/>
</td></tr></table>

The main idea is to use [Microsoft Face API](https://docs.microsoft.com/azure/cognitive-services/face/overview/?wt.mc_id=crpyface-github-dmitryso) to extract coordinates of key points of the face - so called **Face Landmarks**. We then then use OpenCV machinery to apply some transformations to the image according to those key points. In the example above you can see several images blended together, aligned to the eyes.

This technique was originally proposed by [Dmitry Soshnikov](http://soshnikov.com) and called **Cognitive People Blending**. If you develop something substantially interesting, please share your results/feedback/ideas [with him](http://facebook.com/shwars).

<a href="https://notebooks.azure.com/import/gh/CloudAdvocacy/CreepyFaces"><img src="https://notebooks.azure.com/launch.png" /></a>

## How to use this tutorial

This repo contains the following files with demo code:
* [CreepyFace-Tutorial.ipynb](CreepyFace-Tutorial.ipynb) -- Main tutorial code in Jupyter Notebook format
* [CreepyFace-Tutorial-mPyPl.ipynb](CreepyFace-Tutorial-mPyPl.ipynb) -- The same tutorial code, but written using [mPyPl](http://shwars.github.io/mPyPl) library for monadic data processing in Python. If you would like to explore some innovative approach for data manipulations - have a look at it. Reading [mPyPl Tutorial](http://shwars.github.io/mPyPl/tutorial/) before is recommended.
* [ImageGatherer.ipynb](ImageGatherer.ipynb) - some code to use [Bing Image Search](https://docs.microsoft.com/azure/cognitive-services/bing-image-search/index/?wt.mc_id=crpyface-github-dmitryso) to download images results from keywork search.

You should probably start with **CreepyFace-Tutorial**. You can do it in one of the following ways:

* **Recommended** [Clone the repo in Azure Notebooks](https://notebooks.azure.com/import/gh/CloudAdvocacy/CreepyFaces), and then run the code in the cloud
* Clone the repo using `git clone`, and use localy installed Jupyter to run it

## Obtaining Face API keys

To extract Facial Landmarks and call Face API, you would need a special key. You can obtain the key in one of the following ways:

To use Face API, we need to provide a key and endpoint URL (because it is available in different regions, URL can be different). There are many ways to obtain Face API Key:

* If you have an Azure Subscription, the best option is to [create Cognitive Services resource](https://docs.microsoft.com/en-us/azure/cognitive-services/cognitive-services-apis-create-account/?wt.mc_id=crpyface-github-dmitryso), and grab key/url from there
* You can always [create free trial subscription](https://azure.microsoft.com/free/?wt.mc_id=crpyface-github-dmitryso) (you would need a credit card for that)
* If you do not have an Azure Subscription, you can try Face API for free - request your trial key [here](https://azure.microsoft.com/try/cognitive-services/my-apis/?api=face-api&wt.mc_id=crpyface-github-dmitryso).

Once you get the key and the endpoint, please paste them into appropriate place in the code.

## Getting Images 

Whichever way you chose, you would need some images to play with. While we provide some pictures to start with, you may want to:

* Use your own pictures - make sure the face is visible and of reasobable quality / resolution
* Use **ImageGatherer** notebook to get results from Bing Image Search

You would need to upload the images into `images` folder of the notebook directory. In case of Azure Notebooks, this can be done through web interface.

## Sharing Results

We ask you to share the results that you get on social media, so that we can share your joy! Use `#creepyfaces` hash tag, plus the hash tag of the event. In addition, please share the URL with us using the REST function call - sample code is provided in the notebooks.

