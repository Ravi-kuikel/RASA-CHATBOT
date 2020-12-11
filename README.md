# RASA-CHATBOT by Ravi sharma(B170018CS)
CHATBOT FOR RESTAURANT SUGGESTION USING ZOMATO API

Note-This is only a short version of the chatbot.
    -Not yet deployed on any server.
    -completed just in time in 1 day due to some avoitable problems.

REQUIREMENTS-1.RASA(2.1.3)
             2.PYTHON INTERPRETER(HIGHER THAN 3.0)
             3.RASA X(NOT COMPULSORY)
             4.ZOMATO API KEY
             4.requests module for requesting information from zomato.

NOTE:PYTHON CODE FOR REQUESTING INFORMATION FROM ZOMATO IS IS actions folder.

Problem Statement
Developed a chat bot system which will generate top restaurants for a particular cuisine and location. It is based on RASA framework. 


OVER VIEW OF RASA FRAMEWORK:
1.RASA NLU IS FOR INTERPRETING THE INTENT OF THE USER.
3.RASA CORE PERFORMS ACTIONS.

HOW TO TRAIN THE MODEL:
1.rasa train.
2.rasa interative(This can used to update stories and responses).

HOW TO RUN:
FIRST RUN rasa run actions inside action folder.
USING:1:rasa shell.
      2:rasa x
      
RASA NLU:
RASA NLU has two main important functions to do; to look for the intent and entities provided by the user in the message. Intent is what the user is looking for or the purpose of using the chat bot. It can be simple "hi", "goodbye" or in our case "restaurant search". Entities are the information provided by the user which will help to solve the query. In our case it is location where the user wants to search and cuisine what the user wants to eat.

For training the RASA NLU, two files are needed; nlu.ymlL and config.yml.

nlu.yml
Here we define all the intents, the examples for training so that the RASA NLU will be abe to detect the user intent and entitites.

RASA Core:
It can be thought of as dialogue management system. It decides what actions needed to be taken and what message to be replied back to the user.

For training the model domain.yml, stories.md and policy.yml files are needed .

Domain.yml: It contains the all the things the bot should know.
Slots: Acts as bot memory. Store the useful information like location, cuisine from the query sent by the user.

Actions: What action needs to be taken next.

Templates: The text that will be replied back to the user.

Stories.yml:
It contains paths that the conversation can takes place. More you defined the paths, more the better.
