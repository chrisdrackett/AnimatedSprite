# AnimatedSprite

[![Badge License]][License]

Animated sprites library for the **[PlayDate]**.

https://github.com/user-attachments/assets/25133e61-5a49-4dd2-8fa3-cfc153bf230c

<br>
<br>

[![Button Installation]][Install]<br><br>
[![Button Documentation]][Wiki]<br><br>
[![Button Performance]][Performance]

<br>

## Features

_How the sprites class has been extended:_

- **Sprite animations**

- **Finite State Machine**

- **JSON Configuration**

<br>
<br>

## Showcase

_A small example how you could use it:_

```lua
import 'AnimatedSprite.lua'

-- Loading imagetable from the disk
imagetable = playdate.graphics.imagetable.new('path')

-- Creating an AnimatedSprite instance
sprite = AnimatedSprite.new(imagetable)

-- Adding custom a animation state (Optional)
sprite:addState('idle',1,5,{ tickStep = 2 })

-- Playing the animation
sprite:playAnimation()
```

<br>
<br>

## Editor type support

The library includes LuaLS annotations for `AnimatedSprite`, its constructors,
instance methods, and inherited Playdate sprite methods. Install the
[Playdate LuaCATS definitions](https://github.com/notpeter/playdate-luacats) and
include them in your LuaLS `workspace.library` setting; they provide the `_Sprite`
and `_ImageTable` types used by these annotations.

LuaLS infers the instance type without an explicit `---@type` at the call site:

```lua
local imagetable = assert(playdate.graphics.imagetable.new('path'))
local sprite = AnimatedSprite.new(imagetable)
sprite:playAnimation()
sprite:moveTo(200, 120)
```

## Contacts

[![Button Telegram]][Telegram]   
[![Button Discord]][Discord]   
[![Button Mail]][Mail]

<br>

<!----------------------------------------------------------------------------->

[Telegram]: https://t.me/whitebrim
[Playdate]: https://play.date/
[Discord]: https://discordapp.com/users/241961053578199040
[Wiki]: https://github.com/Whitebrim/AnimatedSprite/wiki
[Mail]: mailto:dev@brim.su
[Performance]: Documentation/Performance.md
[Install]: Documentation/Installation.md
[License]: LICENSE

<!----------------------------------[ Badges ]--------------------------------->

[Badge License]: https://img.shields.io/badge/License-MIT-ac8b11.svg?style=for-the-badge&labelColor=yellow

<!---------------------------------[ Buttons ]--------------------------------->

[Button Documentation]: https://img.shields.io/badge/Documentation-0099E5?style=for-the-badge&logoColor=white&logo=GitBook
[Button Installation]: https://img.shields.io/badge/Installation-EF2D5E?style=for-the-badge&logoColor=white&logo=DocuSign
[Button Performance]: https://img.shields.io/badge/Performance-428813?style=for-the-badge&logoColor=white&logo=GoogleAnalytics
[Button Telegram]: https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logoColor=white&logo=Telegram
[Button Discord]: https://img.shields.io/badge/%40brim__-5865F3?style=for-the-badge&logoColor=white&logo=Discord
[Button Mail]: https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logoColor=white&logo=Gmail
