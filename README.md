# DazUERig
Rename - Remove - Reparent Daz bones to use Unreal Engine manneguin animations

Setting up the DazToUnreal plugin:

I recomend setting up the plugin as a project plugin instead of an engine plugin.

This way if the skeleton get messed up it only effects this project not all the projects that use DaztoUnreal

First make sure the project closed before adding the plugin.

In your project's game folder create a new folder and name it Plugins

![Imgur](https://i.imgur.com/DNGWfkD.png)

Find the DazToUnreal Plugin folder

The default path is C:\Program Files\Epic Games\UE_4.25\Engine\Plugins\Marketplace

![Imgur](https://i.imgur.com/aQj1gof.png)

Copy and Paste the entire folder into your project's Plugins folder

![Imgur](https://i.imgur.com/Oz1Yf7e.png)

Add an Unreal Engine animation pack and find the skeleton rig that is used for those animations

![Imgur](https://i.imgur.com/c6BGS8B.png)

In your Project Settings under Plugins - Daz To Unreal Engine Settings change the Genisis 3 and Genesis 8 Skeletons to the same skeleton as the animations

![Imgur](https://i.imgur.com/2h3IFOe.png)

Running the script:

Either download the DazUERig script or clone a copy to your computer.

In Daz Studio enable the ScriptIDE tab by going to Windows - Panes(Tabs) - and click ScriptIDE

In the ScriptIDE tab click File - Open Script and browse to the DazUERig.dsa file and open

Once your character is setup and selected click Execute

![Imgur](https://i.imgur.com/eUqFAwn.png)

This will rename, relabel, remove, and reparent all the necassary bones to make the Daz Skeleton compatible with the UE mannequin rig.

Make sure your character is selected and SendToUnreal

You may want to set up a new Intermediate Folder so that you don't overwrite existing exported characters.

![Imgur](https://i.imgur.com/hymPiaF.png)

Once imported open an UE animation and change the Preview Mesh to your character

This will happen:

![Imgur](https://i.imgur.com/3r4Erfn.png)

In the Asset Details tab - Additive Settings change the Additive Anim Type to Mesh Space

![Imgur](https://i.imgur.com/w9Hi0AS.png)

Things should be looking better now.

In the Skeleton Tree Tab - Options Check Show Retargetting Options

![Imgur](https://i.imgur.com/6JQKLQa.png)

You may need to adjust for animation to work correctly.

ToDo - Add suggested settings

Editing Script For Your Own Needs:

At the bottom of the script (after line 250) is where the Main Program starts

The script uses the bone NAME not the bone LABEL and they are case sensitive

To find the bone name click on it in the scene tree view. In the Node tab you will see the bone Name and its Label

![Imgur](https://i.imgur.com/bZgXdxE.png)
