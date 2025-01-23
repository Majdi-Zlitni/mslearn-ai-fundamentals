---
lab:
    title: 'Analyze text in Azure AI Foundry portal'
---

# Analyze text in Azure AI Foundry portal

Natural Language Processing (NLP) is a branch of AI that deals with written and spoken language. You can use NLP to build solutions that extract semantic meaning from text or speech, or that formulate meaningful responses in natural language.

Azure AI Language Service includes text analysis and NLP capabilities. These include the identification of key phrases in text, and the classification of text based on sentiment. For example, suppose the fictitious travel agent Margie's Travel encourages customers to submit reviews for hotel stays. You could use the Language service to identify key phrases, determine which reviews are positive and which are negative, or analyze the review text for mentions of known entities such as locations or people.

In this exercise, you will use Azure AI Language in Azure AI Foundry portal, Microsoft's platform for creating intelligent applications, to analyze hotel reviews. You'll use the Language service to understand whether the reviews are mostly positive or negative.

## Create a project in Azure AI Foundry portal

1. In a browser tab, navigate to [Azure AI Foundry](https://ai.azure.com?azure-portal=true).

1. Sign in with your account. 

1. On the Azure AI Foundry portal home page, select **Create a project**. In Azure AI Foundry, projects are containers that help organize your work.  

    ![Screenshot of Azure AI Foundry home page with create a project selected.](./media/azure-ai-foundry-home-page.png)

1. On the *Create a project* pane, you will see a generated project name, which you can keep as-is. Depending on whether you have created a hub in the past, you will either see a list of *new* Azure resources to be created or a drop-down list of existing hubs. If you see the drop-down list of existing hubs, select *Create new hub*, create a unique name for your hub, and select *Next*.  
 
    ![Screenshot of the create a project pane with automaticly generated names for hub and project.](./media/azure-ai-foundry-create-project.png)

> **Important**: You will need an Azure AI services resouce provisioned in a specific location to complete the rest of the lab.

1. In the same *Create a project* pane, select **Customize** and select one of the following **Locations**: East US, France Central, Korea Central, West Europe, or West US to complete the rest of the lab. Then select **create**. 

1. Take note of the resources that are created: 
- Azure AI services
- Azure AI hub
- Azure AI project
- Storage account
- Key vault
- Resource group  
 
1. After the resources are created, you will be brought to your project's *Overview* page. On the left-hand menu on the screen, select **AI Services**.
 
    ![Screenshot of the left-hand menu on the project screen with AI Services selected.](./media/azure-ai-foundry-ai-services.png)  

1. On the *AI Services* page, select the *Language + Translator* tile to try out Azure AI Language and Translator capabilities.

    ![Screenshot of the Language and Translator tile selected on the AI Services page.](./media/language-translator-tile.png)   

## Analyze reviews with Azure AI Language

Let's use the information extraction functionality of Azure AI Language to analyze reviews.

1. On the *Language + Translator* page, scroll down and select **Extract information** under *Explore Language capabilities*. Then select the **Other language capabilities** tile.

1. You will be taken to the **Language Studio** at [https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true) and need to sign in.

1. When prompted with **Select an Azure resource**, make the following configurations:
    - **Azure directory**: *Default Directory, the directory you are using*
    - **Azure subscription**: *Select the subscription you are using*
    - **Resource type**: Azure AI services
    - **Resource name**: *select the resource you just created*

Then select **Done**.

> **Note**: If you are ***not*** prompted to choose a language resource, it may be because you have multiple Language resources in your subscription; in which case:
> 1. On the bar at the top if the page, select **Settings (&#9881;)**. 
> 1. On the **Settings** page, view the **Resources** tab.
> 1. Select the resource you just created, and select **Switch resource**. Ensure Managed identity is **Enabled**.
> ![Enable language resource.](media/analyze-text-language-service/language-resource-enabled.png)
> 1. At the top of the page, select **Language Studio** to return to the Language Studio home page.

1. On the **Welcome to Language Studio** landing page of the [Language Studio](https://language.cognitive.azure.com?azure-portal=true), select the **Classify text** tab, then select the **Analyze sentiment and mine opinions** tile. 

1. Under *Select text language*, select **English**.

1. Under *Select your Azure resource*, select your resource.

1. Under *Enter your own text, upload a file, or use one of our sample texts*, copy and paste the following review:

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. Check the box to acknowledge that the demo will incur usage and may incur costs, and then select **Run**.

1. Review the output. Notice that the *document* is analyzed for sentiment, as well as each *sentence*. Select **Sentence 1** to show the sentiment analysis for that sentence. 

Notice that there is an overall sentiment followed by scores next to three categories, *positive score*, *neutral score*, *negative score*. In each of the categories, a score between 0 and 1 is provided. These confidence scores indicate how likely the provided text is a particular sentiment. 

Select **Sentence 1** again to close.

1. Scroll up to select **Clear text box**, and copy and paste the following review:

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```
    
    
1. Select **Run**. Review the output and review the sentiment and confidence level.

1. Select **Clear text** box again, and copy and paste the following review:

    >Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget

1. Select **Run** and review the sentiment together with the confidence level. Have a look at the text and compare the text to the sentiment analysis that the service returned.

In this exercise you used Language Studio to either create a new Language resource or use an existing Language resource. You enabled the resource in Settings before trying out the Sentiment and opinion mining service. You then tested the service with three pieces of text.

## Clean up

If you don’t intend to do more exercises, delete any resources that you no longer need. This avoids accruing any unnecessary costs.

1. Open the **Azure portal** at [https://portal.azure.com](https://portal.azure.com) and select the resource group that contains the resource you created.
1. Select the resource and select **Delete** and then **Yes** to confirm. The resource is then deleted.

## Learn more

To learn more about what you can do with this service, see the [Language service page](https://learn.microsoft.com/azure/ai-services/language-service/overview).
