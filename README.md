# BB-s-Infinite-Fusion-Mod-Menu
## Description:
<p>This Mod adds a Mod Menu aswell as a bunch of Resources that many of my Mods need to the Game.</p>
<p>To Open the Mod Menu, simply open up the pause menu and press "Left".</p>
<p>To exit, press "Cancle", "Right" or "Left" again ("Right" will bring you back to the Pause Menu, "Left and Cancle will leave the Menu completly")</p>

<p>This is meant to be a Framework for other Mods, it comes with one Mod preinstalled (Access PC from anywhere).</p>
<p>Mods that need the Mod Menu to work:</p>
<li>BB's Ability Randomizer (https://github.com/BuezliBueb/BB-s-Infinite-Fusion-Ability-Randomizer)</li>
<li>BB's Quality of Life Cheats (Not on GitHub yet)</li>
<li>BB's Very Hard Difficulty (WIP)</li>
<li>BB's BodyPress & Co (WIP)</li>
<br>

![infiniteFusionModMenu-ezgif com-crop](https://github.com/BuezliBueb/BB-s-Infinite-Fusion-Mod-Menu/assets/164735539/d08ca695-c40d-4a44-8f93-d56ea3bf3199)

## Install/ Uninstall:
<p>Simply drag the Contents into your Folder that contains "Game.exe"</p>
<p>To uninstall, Navigate to Data/Scripts/998_mods and remove the following files: [001_BB_Mod_GameDataRegistry.rb, 001_UI_ModMenuCommands.rb, 099_BB_Mod_LoadRegistry.rb, 002_BB_ModMenu]</p>
<p>Warning: Removing the above Mentioned Files without removing any Mod depending on them will cause your game to Crash.</p>
<br>

## For Modders:

<details>
<summary>Adding your own mods to the Mod Menu</summary>
<p>To register your Options in the Mod Menu, add the Following code:</p>
<pre>
  <code class="language-ruby">
ModMenuCommands.register("YourIdHere",{
    "parent"      => "main",
    "name"        => _INTL("The name you want displayed"),
    "description" => _INTL("The Description you want displayed"),
    "effect"      => proc{
      #Write your Code Here 
    }
  }
)
  </code>
</pre>
<p>To add a menu with a submenu:</p>
<pre>
  <code class="language-ruby">
ModMenuCommands.register("YourIdHere",{
    "parent"      => "main",
    "name"        => _INTL("The name you want displayed"),
    "description" => _INTL("The Description you want displayed"),
  }
)
ModMenuCommands.register("YourSubIdHere",{
    "parent"      => "YourIdHere",
    "name"        => _INTL("The name you want displayed"),
    "description" => _INTL("The Description you want displayed"),
        "effect"      => proc{
      #Write your Code Here 
    }
  }
)

  </code>
</pre>
</details>
