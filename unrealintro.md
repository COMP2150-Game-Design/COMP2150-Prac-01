# Week 01 - Intro to Unreal and Toy Analysis

![TODO: An overview of the whole intro level map.]()

Welcome to the COMP2150 Pracs! In these pracs, you'll be working on the digital side of game design: building levels, prototypes and games as you work towards your two major assessments.

Today's class will be focused on getting familiar with Unreal Engine by way of exploring the game you will be building a level for for the first assignment. Your prac demonstrator will be going over slides and directing activities throughout the lesson, while this sheet will serve to give you further details as you go.

Don't hesitate to speak up if you are stuck or unsure about anything! GLHF!

By the end of this worksheet, you should:

* Have your GitHub account linked to your Student ID.
* Know how to clone, commit and push to GitHub repos.
* Understand how to edit Unreal Engine levels.

## Assignment deliverable
Today you will be analysing the core toy of the game you will be working on for the level design assignment: CryoShock. The notes, insights and artefacts you make today will help you build your levels more thoughtfully.

## Task 0: Acknowledgements and Ice-Breakers (5 min)
Your instructor will run through any acknowledgements and ice-breakers with you as a class to ensure you are familiar with your peers.

## Task 1: GitHub and GitHub Classroom (10 min)

### Linking your account and Student ID

When you clicked the link to accept this task, you would have been prompted to select your Student ID from a roster that looks something like this:

![Image of the roster](images/selectnumber.png)

This roster is for <b>this unit only</b> and links your GitHub account, meaning we are able to quickly access your work. This will be important for pracs and submitting your assignment.

If you did not select your Student ID, don't worry. You'll be able to select it next week when you accept that week's lab. If you couldn't find your Student ID, you'll need to contact the staff to have your ID added to the roster before you can select it.

<b>Make sure you've connected your account to your Student ID before the Level Design assignment is due! Failure to do so may result in your assignment not being marked!</b>

### Cloning your repo
Clone this repo onto your work station. Officially, we support GitHub Desktop in this unit, but you can use any GitHub client you'd like.

To clone a repository, open up the GitHub Desktop app. Then, select File > Clone Repository. You should be able to find your repo under the "GitHub.com" tab. If not, you can copy and paste the URL to the repo instead. Remember to save onto the hard-drive, not the Claudius drive.

For more detailed instructions, ask your instructor or refer back to your COMP1151 notes. Remember to note where you are saving your repo!

![Image of the clone button](images/cloning.png)

## Task 2 Opening the project (5 min)
The repo contains an Unreal Engine project. To open the project, first open Unreal Edtior. If you are working on your own device, you will instead need to open the Epic Games Launcher.

### Opening Unreal
From here, open Unreal Engine 5.7.x. If you don't have it installed on your computer, you'll need to do so now. Make sure you areu sing Unreal Engine 5.7.x. Anything below or above 5.7 will not work. The final number denotes a hot fix, and there is general compatibility between these verisons (e.g., 5.7.1 and 5.7.2). Follow the prompts for installing and creating an account/logging in.

### Opening the project
You then want to open the project by pressing File > Open Project > Browse and heading to the folder you saved the repo into, then Prac 01 Unreal Project > COMP2150_LDTemplate.uproject.

If you're struggling with this step, don't get frustated. Call over your instructor to give you a hand.

When the project opens up, you should be inside the map called Lvl_Intro. You're ready to go!

![TODO: An image of the sample scene.]()

## Play and discuss (15 min)
Now it's time to play Cryoshock! A small intro level has been created for you to introduce you to the game's core mechanics. You can run the game by pressing the Green play button at the top of the viewport.

Before you dive in, the controls are:

| Key  | Action |
| ------------- | ------------- |
| WASD  | Move  |
| Mouse movement  | Look  |
| Space bar | Jump |
| Left click (hold and release) | Blink (when unlocked)|
| Right click (hold) | Activate shield (when unlocked)|
| R | Respawn |
| Esc| Closes the game|

As you play through the game, consider the following:

* What kind of game is this? What genre terms would you use to describe it?
* Considering this game through the lens of playful design, what opportunities of for play are present here?
* What questions do you have about the mechanics? Try thinking about them in terms of "what happens when..."?

Try chatting through these with the students around you once you've had a run through or two. Your instructor will work with you on sharing your ideas and observations.

## Mechanic and Dynamics analysis (30 min)
Your instructor will place you in small groups and assign you one of the following mechanics:

* Running and jumping
* Moving Platforms
* Doors and Switches
* Spike Pits
* Blinking
* Cryo Fields
* Turrets
* Shields

Your job is to experiment with this mechanic and analyse:

* What is the purpose of this mechanic? What does it afford the player to do? How does it challenge them?
* What are its paramters that you can change as a level designer? What happens when you take these to the extreme?
* How does this mechanic interact with others? What happens when you combine them unexpected ways (spatially, or by combining objects)?

To figure this out, you'll need to start editing the level and modifying objects in your scene. Your instructor won't go over this on the board, so check these two sheets to help you:

* [Intro to editing in Unreal](unrealintro.md)
* [Documentation on mechanics](mechanics.md)

Call over your instructor if you need help, and collaborate in your groups!

Make sure someone is writing down your findings/observations, and that you are preparing a small demo to show your peers.

### Saving, committing and pushing your work
Don't forget to save, commit and push your work. This was a good habit to get into in COMP1151, and a good one to stick with this semester! Call over your instructor if you've forgotten how to do this.

## Sharing our work (20 min)
Your instructor will direct you on sharing your work with your peers. Get ready to show your work to others and have them play, critique and add to your discoveries.

When playing the work of others and listening to their observations, remember to respond with respect: feedback should be constructive and encouraging, not contrary and diminishing.

### Reflect & Iterate
With the remaining time, think about what you've learnt from others and how this can apply to what you created. Did it change the way you thought about the mechanics you were investigating? If you knew that earlier, how might it have changed what you did in this class?

## Next Week
Next week, we will be building some challenges and iterating on them with this toolkit. You'll be creating a whole new repo next week, so don't worry about blowing stuff up in this one! Also, if you've found any bugs, please let Cam know by posting on the iLearn forums so we can fix them (or mournfully explain why we can't!).