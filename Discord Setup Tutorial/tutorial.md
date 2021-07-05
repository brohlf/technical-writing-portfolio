# Discord Setup for Dungeons & Dragons

## Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [1. Create Your Server](#serverCreation)
- [2. Create Your User Roles](#createRoles)
- [3. Create Your Channels](#createChannels)
- [4. Get Your Music Bot](#inviteGroovy)
- [5. Next Steps](#nextSteps)


## Introduction <a name="introduction"></a>



## Prerequisites <a name="prerequisites"></a>
You need to have the Discord app installed, and you need to have an account. If you need assistance with either of these steps, consult Discord's guide to [Getting Started](https://support.discord.com/hc/en-us/articles/360033931551-Getting-Started). That process will only take a few minutes.

System requirements can be found [here](https://support.discord.com/hc/en-us/articles/213491697-What-are-the-OS-system-requirements-for-Discord-). (You'll need about 65 MB of available hard drive space.)

If you're configuring a server that you don't own, you'll need the *Manage Server* permission on that server. Otherwise, no experience with Discord beyond installation and account creation is necessary.


## 1. Create Your Server <a name="serverCreation"></a>
Time to create your server. This is where you will be hosting your games. It'll be a bit lonely at first, but soon it will be full of friends! 

**Follow along** - this will be quick and easy!

![create-server-example](https://user-images.githubusercontent.com/79812580/124398371-ff59f980-dcda-11eb-8aee-b27b4eb8fe92.gif)

**Note:** Don't worry about server templates for now. They won't help with what we're doing.


## 2. Create Your User Roles <a name="createRoles"></a>
Let's navigate into your server settings and create some user roles. We'll make one for GMs, and one for players. Later, there will be one for your music bot too. Roles enable you to create profiles of server permissions. Permissions determine how much freedom and control user have in your server. As the owner of this server, you permanently have administrator permissions - they can't be taken away from you, even by others with administrator privileges. Ownership is not a role. We'll deal with both roles and permissions in this section.

### 2.1. Roles

**Follow along** - let's start with a role for GMs.
![create-role](https://user-images.githubusercontent.com/79812580/124400490-68943980-dce8-11eb-84fa-e4e7c3848169.gif)

Repeat this process to create a "Player" role.

#### 2.2.1 Assigning Roles
Before we move on to configuring permissions, you need to know how to assign roles. Just right click on a user's name and navigate to the roles options.

<img width="1549" alt="assign-roles" src="https://user-images.githubusercontent.com/79812580/124401107-42bd6380-dced-11eb-8c0c-9339bfb553d7.png">

### 2.2. Permissions

**Follow along** - let's navigate to the permissions tab
![navigate-permissions](https://user-images.githubusercontent.com/79812580/124401060-c7f44880-dcec-11eb-835b-a011212ad3a6.gif)

We won't go into detail, explaining what all of these permissions do. Basically, players need the ability to move around and speak in your social channels. And GMs need the ability to speak over people, mute people, move players around, and even kick or ban players that are causing problems. Just make sure that you configure your GM and Player permissions to look like this.

[permissions-gm]: https://github.com/brohlf/technical-writing-portfolio/blob/main/Discord%20Setup%20Tutorial/images/permissions-gm.png
[permissions-players]: https://github.com/brohlf/technical-writing-portfolio/blob/main/Discord%20Setup%20Tutorial/images/permissions-players.png

| gm permissions      | player permissions      |
:---------------------|-------------------------:
| ![][permissions-gm] | ![][permissions-players] |



## 3. Create Your Channels <a name="createChannels"></a>
Now that we have your roles created, let's create some channels! You'll need a text channel for communicating with your Groovy bot, and you'll need an additional voice channel for speaking with individual players privately during games.

Just to the right of "TEXT CHANNELS", click on the plus icon, shown below.

<img width="446" alt="create-channel-button" src="https://user-images.githubusercontent.com/79812580/124401343-85337000-dcee-11eb-97c0-5590670978bf.png">

You should then see this popup. Make sure the channels isn't private. Click "Create Channel."
<!-- might be able to remove this, but be sure to expand description -->
<img width="500" alt="new-channel-popup" src="https://user-images.githubusercontent.com/79812580/124408873-cd618b00-dd0c-11eb-8d32-cd20e91f0bbb.png">

Repeat that process to create a new voice channel for private chats with players during games.

You can also rename that general voice channel by navigating to it's "edit channel" page. Click on the gear icon to the right of the channel name.

<img width="341" alt="edit-channel" src="https://user-images.githubusercontent.com/79812580/124409763-8e343980-dd0e-11eb-8c10-8f0669fd387c.png">

Once you've made you're change, clikc on the green "Save Changes" button that will pop up at the bottom of the page.

Then, you can edit the channel name.

When you're should then see these two new channels!

<img width="324" alt="new-channels" src="https://user-images.githubusercontent.com/79812580/124408807-a3a86400-dd0c-11eb-8f64-e0267c51f393.png">


## 4. Get Your Music Bot <a name="inviteGroovy"></a>

[Groovy Bot](https://groovy.bot/)

<img width="495" alt="permissions-groovy" src="https://user-images.githubusercontent.com/79812580/124401866-c5e0b880-dcf1-11eb-8e45-f45c17c6685b.png">

<img width="1411" alt="add-to-discord-button" src="https://user-images.githubusercontent.com/79812580/124402080-65527b00-dcf3-11eb-82cf-daa5d459d8b8.png">


you need to grant admin privileges so that Groovy can create a role for itself. But, once it's done that, you should revoke admin privileges.
<img width="544" alt="grant-admin-privilages" src="https://user-images.githubusercontent.com/79812580/124402044-27eded80-dcf3-11eb-8891-b670f6644e57.png">



![navigate-channel-permissions](https://user-images.githubusercontent.com/79812580/124403395-d7c75900-dcfb-11eb-8671-35882ed5976e.gif)

<img width="740" alt="groovy-channel-player-permissions" src="https://user-images.githubusercontent.com/79812580/124403455-25dc5c80-dcfc-11eb-9b59-ed72219c187d.png">


<img width="343" alt="channel-permission-explanation" src="https://user-images.githubusercontent.com/79812580/124403397-da29b300-dcfb-11eb-8982-8b3f703b383c.png">


[Groovy Commands](https://groovy.bot/commands)


when you pause groovy, you need to explicitly unpause it. Using the play command again won't work.
you'r most frequently used commands will be /play, /pause, /unpause, and /clear


## 5. Next Steps <a name="nextSteps"></a>
avrae dice rolling bot
[inviting friends](https://support.discord.com/hc/en-us/articles/204155938-How-do-I-invite-friends-to-my-server-)
