# IMAGE GENERATOR SCRIPT USING PYTHON AND DALL-E and GPT-3 / DALL-E Playground
> This script uses the GPT-3 text completion models to generate a prompt that is then used to generate images. The results were interesting...


DALL-E based AI vs human images guessor (WIP). Currently, repo only contains a simple script that uses the openai ada Completion model (can easily interchange among curie, davinci, babbage) to generate prompt to generate the images which can then be used to experiment and have fun generating images . The current script can easily be used to create a continuous story with images with a few simple tweaks (an example is contained in the story.py file). However, the goal is to ultimately have a guessing game of whether an image is ai or human-based with two modes:
-  1) implement simple image classification model and used the model to have mode where AI guesses (drag and drop/upload image) and then allow user to confirm whether or not they know if it is AI-generated or human-generated.  Will then use this data to improve the image classification model.
-  2)  allow humans to play a game and let them guess. This can give a neat statistic on quality of DALL-E images produced and how easy it is for humans to tell them apart.

## Built With
- Python
- OPENAI API

## Live Demos
None at the moment, but may do an application that makes user guess between two images whether they are AI generated or taken by, edited by or created by a human

## Getting Started
To get a local copy up and running follow these simple example steps.

### Prerequisites
- An [OPENAI](https://openai.com/api/) - You can sign up from this page
- An Open AI Secret/API key [Generate Key from this page](https://beta.openai.com/account/api-keys). Make sure you store and copy the key somewhere safe.
- It is not necessary to specify organization key but if you are a part of many organizations you should uncomment the line `openai.organization = ""` and specifiy the organization key. You can get org key from this page once logged in: https://beta.openai.com/account/org-settings

### Setup
- Create a .api_key file and paste the api key generated above into file

### Install
- To install relevant packages run following command: `pip install -r requirements.txt`
- [OPTIONAL] if you added packages to the project run following command to update requirements.txt (install pipreqs and pip-tools packages first): `pipreqs --savepath=requirements.in && pip-compile`

### Usage
- You may edit the number of images generated by changing the `NUM_IMAGE` constant
- If you want to edit the prompt to generate text for the image prompt you can change it by chnaging the `PROMPT_FOR_TEXT` constant
- I you would like to change image quality, you can do so by changing the `IMAGE_SIZE` contant. Please note you have a choice among 3 sizes: `1024x1024`, `512x512`, and, `256x256`
- You can also change the model the text is generated from by changing the `TEXT_MODEL` constant. By default, it's the fastest (and cheapest) mode, `ada`
- The `intial_prompt` is not necessary, you can always edit the code to exclude or change it to something different. I simply wanted to have a kitten drinking coffee to be my first image :)
- You will get a resulting `images.csv` from the script that can be used to see the prompts generated for the image and the resulting image url. You may change the name by changing the `FILE_NAME` constant in code
- You can make this script cleaner and abstract it even more with the image generation piece of code: I was more testing out the models going for functional over clean. I'd also implore you to experiment changing the text prompt based on some additional elements or maybe making use of a previously generated prompt to generate the next one. You may observe some patterns and you may even have some fun playing with these models while you're at it.

### Run tests

### Deployment
run `python3 main.py` or   `python main.py` depending on system

## Troubleshooting
if you get the following error message when you run the script:
`openai.error.InvalidRequestError: Billing hard limit has been reached` it means your free trial period is over and that you need to set up payment to generate images. <br>
Go to the following links for more info: <br>
- [General OpenAI pricing](https://openai.com/api/pricing/) ( You'd more be concerned with the Image Model pricing)
- [Set up Billing information and usage limits](https://beta.openai.com/account/billing/overview)

If you do not have ability to pay for images (and you have already used up your free credts or they are expired), I unfortunately can't help you since the Image model is on a pay per use basis.

## Some Results
![1](https://user-images.githubusercontent.com/31193823/209407145-b03e903b-5160-438f-b099-00edf693f770.png) <br>Prompt: a high quality studio photo of a kitten drinking coffee - Not model generated prompt<br><br>
![4](https://user-images.githubusercontent.com/31193823/209407165-7b1cd1c3-e219-4b78-b924-1b66c6299d18.png) <br>Prompt: of your great grandmother; or a photo of a grandparent (e.g - Model generated prompt (ada)<br><br>
![5](https://user-images.githubusercontent.com/31193823/209407205-580f63f4-5a23-46fa-8924-5ea2a7c639a1.png) <br>Prompt: " of a gift basket, to describe the style that the painter would employ to convey" - Model generated prompt (ada)<br><br>
![images2-7](https://user-images.githubusercontent.com/31193823/209417777-9e92a4b6-7127-425e-9653-a64f4d4270dc.png) <br>Prompt: ", or a stand-in for a painted masterpiece, without as much reason as" - Model generated prompt (ada)<br><br>
![images2-8](https://user-images.githubusercontent.com/31193823/209417795-40f09bfd-10fd-4f8c-8f35-97668d23af7e.png) <br>Prompt: " that portrays a figure of a bal group, a small group of friends, or" - Model generated prompt (ada)<br><br>
![images2-9](https://user-images.githubusercontent.com/31193823/209417799-b1172879-ad0b-43cd-a90f-89aff4689622.png) <br>Prompt: " called “The North-Wind Biogram,” through which some of"  - Model generated prompt (ada)<br>



## References
Learn more about models used here: https://beta.openai.com/docs/introduction

## Authors

👤 **Maya D.**

- GitHub: [@mcrd25](https://github.com/mcrd25)
- LinkedIn: [LinkedIn](https://linkedin.com/in/mayadouglas)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments


## 📝 License
You are not allowed to use images as your own. They belong to owner of account used to generate.

Apologies for any and all typos. This was a really quick project write up
