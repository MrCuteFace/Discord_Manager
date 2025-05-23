Authors:
Gal Elhiani,
Daniel Cohen,
Deep Learning final project
============================================================================================================================================================
Instructions to run the project:
#1
first you must download the discord app if you dont already have it:
https://discord.com/download


#2
create an account:
https://discord.com/register
and log in to your account


#3
enter to the server using the following link: (its not a virus we swear :D):
(removed for privacy purposes)
and change your name to an animal of your choosing (necessary)

#4

you must acquire the following files (which will be shared to the lecturer) here is a checklist in case of missing files (there should be 6 in total):
.env
Deep Learning Discord manage Project.ipynb
discord_commands.jsonl
create_database.ipynb
convert_to_actions.ipynb
bert_discord_model.pth
gpt2_discord_model.pth
(in here included the code files)
#5
make sure the folder: "Discord_Manager_files" has a shortcut within "MyDrive" (necessary)


#6 (optional)
incase to retrain the model you must follow the following steps:
1. first run create_database.ipynb
2. go to convert_to_actions.ipynb and switch Runtime type to gpu (highly recommended)
3. scroll down to the cell under the headline "Training the model and printing its progress:" and change the variable "should_run" to True and execute the entire notebook
4. change "should_run" back to False.


#7
in order actually use the bot you must run the notebook Deep Learning Discord manage Project.ipynb on cpu Runtime type (necessary)
and just run the notebook (Ctrl+F9 in shortcut)


General instructions:
all the commands must be case sensitive for users and roles otherwise it wont recognize neither the users nor the roles correctly.
the bot currently supports only three types of actions: ban, add role and remove role.
(examples in the end)
the inputs and outputs of the bot will be under the channel "dog-testing"
in order to input a command for the bot you must first use "!" at the beginning of each sentence (but not for the confirmation step).
you must use the actual username of the user you would like to perform actions on by pressing on the appropriate user's nickname on the right side of the screen and taking the actual username under the nickname.
the bot will ask for confirmation (yes/no) to your latest input and will wait for 30 seconds, if it doesnt get a confirmation or an input that is not yes/no it will cancel the action.
after confirming the input it will execute the command by itself (please don't ban us)
examples of use:


bambi1826: !bambi1826 is not worthy of chess player role, revoke his role
Dog_Manager: {'action': 'remove_role', 'user': 'bambi1826', 'role': 'chess player'} (yes/no)
bambi1826: yes
Dog_Manager: Action confirmed for bambi1826!
Dog_Manager: Action Done for bambi1826!


User: !bambi1826 is abusing his power please ban him.
Dog_Manager: {'action': 'ban', 'user': 'bambi1826', 'role': 'null'} (yes/no)
User: no
Dog_Manager: Action cancelled for User.


bambi1826: !please add kitten6293 a role of chess player
Dog_Manager: {'action': 'add_role', 'user': 'kitten6293', 'role': 'chess player'} (yes/no)
Dog_Manager: bambi1826, you took too long to respond. Action cancelled.


bambi1826: !please ban kitten6293
Dog_Manager: {'action': 'ban', 'user': 'kitten6293', 'role': 'null'} (yes/no)
bambi1826: blah
Dog_Manager: Invalid response. Please retype the message and answer 'yes' or 'no'.

