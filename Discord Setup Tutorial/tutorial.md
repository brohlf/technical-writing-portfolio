# Discord Setup for Dungeons & Dragons

## Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [1. Create Your Server](#serverCreation)
- [2. Create Your Channels](#createChannels)
- [3. Create User Roles and Configure Permissions](#createRoles)
- [4. Get Your Music Bot](#inviteGroovy)
- [5. Keep Going!](#nextSteps)


## Introduction <a name="introduction"></a>

If you're a game master (GM) and you're running tableop roleplaying games (TTRPGs) virtually, you need a Discord server.
Discord is the most popular tool in the TTRPG space for hosting a gaming community, or even a fanbase. While some of its
essential features can be found on virtual tabletops (VTTs), like Roll20, both Discord's UI and the quality of its services
are superior to what is offered by available VTTs. It's also much more convenient for your community to interact through Discord
than through a VTT, or even through other chat focused apps like Zoom or Teams.

Discord servers are free spaces that provide text, voice, and video chat features. Servers are easy to create, but harnessing their potential can
be a bit intimidating. Your job is already hard enough, and all the time you spend wrangling technology is time you
aren't focusing on the game.

This guide will help you quickly create a a well organized, ready to scale, and invite-only server with a music bot that
you can use to add atmosphere to your games. By the end, you'll also be familiar with all of the essential features of the app.
The best part is that you won't have to go reading about anything in depth.

Note: this is a tutorial. It does not discuss the features of Discord in depth. However, it does touch on a few gotchas so you aren't caught off
      guard in the middle of a game session. For an in-depth explanation of what Discord is, click [here](https://discord.com/safety/360044149331-What-is-Discord)

First, we'll create your server. Then, we'll create a new text channel specifically for communicating with your music bot and a new voice channel
for private chats with players during your games. Then, we'll create some user roles for GMs and Players. Once we have those, we'll configure server
and channel-specific permissions for those roles. Roles are essential to maintaining a well-organized and stable server. As you begin scaling
your community and adding features to your server, you will need more complex roles and permissions. But that's not what this guide is about. In the last section, you'll find a recommendation for a dice rolling bot.

This will take about 25 minutes. Let's get going!

## Prerequisites <a name="prerequisites"></a>
You need to have the Discord app installed, and you need to have an account. If you need assistance with either of these steps, consult Discord's guide to [Getting Started](https://support.discord.com/hc/en-us/articles/360033931551-Getting-Started). That process will only take a few minutes.

System requirements can be found [here](https://support.discord.com/hc/en-us/articles/213491697-What-are-the-OS-system-requirements-for-Discord-). (You'll need about 65 MB of available hard drive space.)

If you're configuring a server that you don't own, you'll need the *Manage Server* permission on that server. Otherwise, no experience with Discord beyond installation and account creation is necessary.


## 1. Create Your Server <a name="serverCreation"></a>
Time to create your server! This is where you will be hosting your games. It'll be a bit lonely at first, but soon it will be full of friends! 

**Follow these steps** to create your server:
<ol>
  <li>
    Click on the "Add a Server" button, represented by a plus icon on left-side menu bar
  </li>
  <li>
    Select "Create My Own"
  </li>
  <li>
    Select "For me and my friends"
    <ul>
      <li>
        Don't worry about server templates for now. They won't help with what we're doing
      </li>
    </ul>
  </li>
  <li>
    Give your server a name, and click "Create"
  </li>
</ol>

**Fig.1** shows what that process looks like.

<p align="center">
  <img src="./images/create-server-example.gif" alt="">
  <b>Fig.1 - Server Creation</b>
</p>


## 2. Create Your Channels <a name="createChannels"></a>
Now that we have your roles created, let's create some channels! You'll need a text channel for communicating with your music bot, and you'll need an additional voice channel for speaking with individual players privately during games.

When you're should then see these two new channels!

<img width="324" alt="new-channels" src="https://user-images.githubusercontent.com/79812580/124408807-a3a86400-dd0c-11eb-8f64-e0267c51f393.png">

### 2.1 Channel Creation
Just to the right of "TEXT CHANNELS", click on the plus icon, shown below.

<img width="446" alt="create-channel-button" src="https://user-images.githubusercontent.com/79812580/124401343-85337000-dcee-11eb-97c0-5590670978bf.png">

You should then see this popup. Make sure the channels isn't private. Click "Create Channel."
<!-- might be able to remove this, but be sure to expand description -->
<img width="500" alt="new-channel-popup" src="https://user-images.githubusercontent.com/79812580/124408873-cd618b00-dd0c-11eb-8d32-cd20e91f0bbb.png">

Repeat that process to create a new voice channel for private chats with players during games.

### 2.2 Renaming Channels
You can also rename that general voice channel by navigating to it's "edit channel" page. Click on the gear icon to the right of the channel name.

<img width="341" alt="edit-channel" src="https://user-images.githubusercontent.com/79812580/124409763-8e343980-dd0e-11eb-8c10-8f0669fd387c.png">

Once you've made you're change, clikc on the green "Save Changes" button that will pop up at the bottom of the page.

Then, you can edit the channel name.


## 3. Create User Roles and Configure Permissions <a name="createRoles"></a>
Let's navigate into your server settings and create some user roles. We'll make one for GMs, and one for players. Later, there will be one for your music bot too. Roles enable you to create profiles of server permissions. Permissions determine how much freedom and control user have in your server. As the owner of this server, you permanently have administrator permissions - they can't be taken away from you, even by others with administrator privileges. Ownership is not a role. We'll deal with both roles and permissions in this section.

### 3.1. Roles

#### 3.1.1 Creating Roles
**Follow along** - let's start with a role for GMs.
![create-role](https://user-images.githubusercontent.com/79812580/124400490-68943980-dce8-11eb-84fa-e4e7c3848169.gif)

Repeat this process to create a "Player" role.

#### 3.1.2 Assigning Roles
Before we move on to configuring permissions, you need to know how to assign roles. Just right click on a user's name and navigate to the roles options. Dont worry about assigning roles to yourself. As the owner, you have permanent admin privileges which cannot be taken away from you.

<img width="1549" alt="assign-roles" src="https://user-images.githubusercontent.com/79812580/124401107-42bd6380-dced-11eb-8c0c-9339bfb553d7.png">

### 3.2. Server Permissions

**Follow along** - let's navigate to the permissions tab
![navigate-permissions](https://user-images.githubusercontent.com/79812580/124401060-c7f44880-dcec-11eb-835b-a011212ad3a6.gif)

We won't go into detail, explaining what all of these permissions do. Basically, players need the ability to move around and speak in your social channels. And GMs need the ability to speak over people, mute people, move players around, and even kick or ban players that are causing problems. Just make sure that you configure your GM and Player permissions to look like [this](https://github.com/brohlf/technical-writing-portfolio/blob/main/Discord%20Setup%20Tutorial/Permission%20Configurations/gm-player-configs.md).


## 4. Get Your Music Bot <a name="inviteGroovy"></a>

Groovy bot is one the most popular music bots for Discord. Music support from VTTs is unreliable, so if you want music in your game, you should have a music bot as backup. This one is especially convenient because all you need to do is give it a link to a youtube or spotify song or playlist and it will do the rest. Bots join your server and behave as members just like people do. The difference is that you communicate with and configure them using text commands. We will confine the groovy bot to the "groovy" channel, so it won't hear any commands entered into the "general" chat. We will also restrict players from typing inthe "groovy" channel. DMs should have exclusive control over the music in their games. Groovy will join you whichever voice channel you are in when you issue a command. It will play music through voice chat just like your players use itto speak. When it's left idle for a while, it will automatically leave voice chat. You cna;t force it to leave.

### 4.1. Invite Groovy Bot

Click the following link to download [Groovy Bot](https://groovy.bot/). Click "Add to Discord" to begin the invititation process.

<img width="1411" alt="add-to-discord-button" src="https://user-images.githubusercontent.com/79812580/124402080-65527b00-dcf3-11eb-82cf-daa5d459d8b8.png">

This will navigate you to a panel that contains a dropdown menu titled "ADD TO SERVER." Select your server name and click continue. You may also need to login.

At this point, you should see this panel. You need to grant admin privileges so that Groovy can create a role for itself. But, once it's done that, you should revoke admin privileges. Click "Authorize."

<img width="544" alt="grant-admin-privilages" src="https://user-images.githubusercontent.com/79812580/124402044-27eded80-dcf3-11eb-8891-b670f6644e57.png">

Now, you should see a new member in your chat! This is groovy bot. But Groovy doesn;t need those admin privileges anymore. Navigate to your list of server roles in server settings. You should see a new role for Groovy. Navigate to the permissions tabs for the "Groovy" role and configure its permissions to match the [following](https://github.com/brohlf/technical-writing-portfolio/blob/main/Discord%20Setup%20Tutorial/Permission%20Configurations/groovy-configs.md).

### 4.2 Configuring Groovy Bot

Now let's restrict Groovy from seeing anything that happens in the "general" text channel. Navigate to the channel settings by clicking on the gear icon to the right of the channel name. We'll modify Groovy's permissions for this specific channel. You'll have to add the groovy role to the list of roles tracked by this channel. At first, you should only see the "@Everyone" role. 

**Follow along**
![navigate-channel-permissions](https://user-images.githubusercontent.com/79812580/124403395-d7c75900-dcfb-11eb-8671-35882ed5976e.gif)

Channel permissions override server permissions. And they take effect only in the server for which they are configured.
You will see a list of permissions each with an x, a slash, and a check next to them. Here's what they mean:
- a: explicitly deny this permission for this server
- b: inherit server permission
- c: explicitly allow this permission for this server
<img width="343" alt="channel-permission-explanation" src="https://user-images.githubusercontent.com/79812580/124403397-da29b300-dcfb-11eb-8982-8b3f703b383c.png">

Explicitly deny all permissions to Groovy in the general channel.

Explictly give players permission to view the channel and to read text history in the Groovy channel.


### 4.3 Using Groovy Bot
[Groovy Commands](https://groovy.bot/commands)


when you pause groovy, you need to explicitly unpause it. Using the play command again won't work.
you'r most frequently used commands will be /play, /pause, /unpause, and /clear


## 5. Keep Going! <a name="nextSteps"></a>
Groovy isn't the only helpful bot! If you aren't using a VTT, but you need a way to roll dice, you can do that right in your server! Invite the "Avrae" bot and create another channel for dice rolling.

As cool as Groovy is, you will eventually want to get some of your real friends into the server. If you need some help with that, follow this short guide to inviting your friends: [inviting friends](https://support.discord.com/hc/en-us/articles/204155938-How-do-I-invite-friends-to-my-server-)

As your community grows, you will need to add more roles, more bots to moderate your users, and more channels.
