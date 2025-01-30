---
lab:
    title: 'Explore generative AI with Microsoft Copilot'
---
# Explore generative AI with Microsoft Copilot

Generative AI describes a category of capabilities within AI that create original content. People typically interact with generative AI that has been built into chat applications. One popular example of such an application is Microsoft Copilot, an AI-powered productivity tool designed to enhance your work experience by providing real-time intelligence and assistance. 

In this exercise, you will use Microsoft Copilot to generate travel plans.

> **Note**: This exercise assumes that you have a [personal Microsoft Account](https://signup.live.com) (such as an outlook.com account) with which you are signed into [Microsoft Edge](https://www.microsoft.com/edge/download) on your computer. If you have both a work account and a personal account, be sure to select your *personal* account in the account settings at the top left of Microsoft Edge.

## Use Microsoft Copilot to generate travel plans

1. In Microsoft Edge, browse to [Microsoft Copilot](https://copilot.microsoft.com) at `https://copilot.microsoft.com`. Click on the **Sign in** button on the right hand side of the screen. Sign in using your personal Microsoft account - closing any welcome messages or offers that are displayed.

    >**Note**: You may be prompted to continue with your **Work** or  **Personal** account. Select **Personal** and sign in. 

>Consider the following ways you can improve the response a generative AI assistant provides:
> - Start with a specific goal for what you want the assistant to do
> - Iterate based on previous prompts and responses to refine the result
> - Provide a source to ground the response in a specific scope of information
> - Add context to maximize response appropriateness and relevance
> - Set clear expectations for the response

1. Let's start with a specific goal. In the chat box at the bottom of the Copilot pane, enter following the prompt:

    ```prompt
    Where are the 10 best places to visit in the world in April?
    ```

1. Review the response from Copilot, which should present a description of places to visit.
 
1. Let's iterate based on previous prompts and responses to refine the result.

1. Enter the following prompt:

    ```prompt
    Can you explain your reasoning for the top three places? 
    ```

1. Review the response, which should explain the reasoning.

1. Now, let's provide a source to ground the response in a specific scope of information. In a web browser, open the image of two people doing yoga [wellbeing.jpg](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/sheryang-ai-foundry/Instructions/Labs/media/wellbeing.jpg) at `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/sheryang-ai-foundry/Instructions/Labs/media/wellbeing.jpg`. 


1. In Microsoft Copilot, select the **+** in the chat box and upload an image. Then enter the following prompt (note: make sure to remove the brakets and type in the top location listed from the previous response to add *context* to the prompt): 
    
    ```prompt
    Where can I do the activity in the photo in [name of location from the previous response]? 
    ```

1. Review the response, which should provide options in the top recommended destination related to yoga. 
    
    >**Note**
    >What do you think will happen if you are not specific about the destination? Try uploading the same yoga photo again, and using the prompt *"Where can I do this acitivty?"* You will likely find that the reponse is not related to your travel destination, because it is missing *context*. 

1. Now let's try to add context to another question and set clear expectations. Enter the following prompt: 

    ```prompt
    What are three hotel recommendations [name of location from the previous response] close to public transportation?
    ```

1. Review the response. Notice at the bottom of the recommendations, you are asked if you would prefer one of the options. Enter the following prompt: 

    ```prompt
    Option 1 interests me
    ```

1. Review the response. Notice that the response is able to build on the previous reponse and provide additional resources. 

1. Enter the following prompt: 

    ```prompt
    Create an image of an invitation for a trip here
    ```

1. Review the response. You may notice that some of the text does not make sense. Why do you think that is? 

    > **Important**: The specific response may vary. The AI-generated response is based on information publicly on the Web. While it can be used to assist you, it is not guaranteed to be 100% accurate and does not replace the need for human review.

1. When you are done, you can close the window. 