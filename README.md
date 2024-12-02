# CorruptedClue (NDS Exploit)
A "Cate West: The Vanishing Files" stack smash exploit for the Nintendo DS that can execute unsigned code from the savegame.

> These are ARM9 exploits that takes over a NDS mode cartridge. These type of exploits are very limited since there's no SD or NAND access. They can be used to run a small payload. These exploits are almost useless, but still fun :)

## Exploit/Vulnerability Detail:
> ## Stack smash via unchecked string-length<br><br>
> *"The savedata contains multiple ASCII strings, mostly for the player slot names and high-score data. The string lengths of these vectors are not checked, so one can use a very large string to overwrite the stack and execute unsigned code."*
>
> This iteration of the exploit only targets the high-score data. I found that working with the high-score data was more beneficial for manipulating the stack, rather than working with the profile slot names. (They are are still exploitable).
###
## Requirements:
* A copy of the `Cate West: The Vanishing Files` NDS game (US Version only).
* Any DS that's in the NDS family (NDS, NDSL, DSi, DSiXL, 3DS, 3DSXL, NEW3DS, NEW3DSXL, 2DS, 2DSXL, etc.)
* A way to inject the save. (DSi users can use [ndsi-savedumper](https://github.com/edo9300/ndsi-savedumper) and 3DS users can use [TWLSaveTool](https://github.com/TuxSH/TWLSaveTool/releases).
###
## Triggering the exploit
* `Touch the Screen to Begin`
* Select the `Quick Play` widget.
* Click `Open`.
###
## Support:
* US version of the game. (EUR version will be supported at a later date)
* Works with emulators. (no$gba, TWiLightMenu++, etc.)
###
## FAQ:
Q: Why another NDS savegame exploit? Aren't they useless?<br>
A: They are indeed useless, but this small project was only for fun and to polish up on reverse-engineering.

Q: What did you learn from exploiting this game?<br>
A: I learned how to "ACTUALLY" reverse engineer the CRC32 algorithm and clean my injected strings to avoid any unnessasary corruptions.

Q: Will you make more of these?<br>
A: Maybe, only time will tell until I get bored again and try to break a game.

Q: What made you choose this game?<br>
A: I bought this at my local library for $3, played the game and found it fun. Then I thought what if I broke it. And here we are :).
###
## Credits:
* [St4rkDev](https://twitter.com/St4rkDev): Original payload code
###
