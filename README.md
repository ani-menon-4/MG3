# MG3
## Devlog
1. The default value for a Float is 0, as is the default value for an Integer. The default value for a String is "". The default value for a boolean is false.
2. The Update method is automatically called every frame. It does not need to be called via code.
3. The KickWeapon class and TimerText class use the timer to limit the duration of the kick being active and indicate how much longer the game will go on for, respectively. Both of these classes use a float variable as an argument for the Timer's BeginTimer() method in order to start the timer at the class's desired duration, and both classes use the Update() method to check whether the timer has finished (via calling the IsFinished() method) every frame.

> From here, the differences between how KickWeapon and TimerText use the timer is that KickWeapon simply disables the KickWeapon if the isFinished() check returns a result of true, whereas TimerText calls an internal method GameOver(), disabling the player and activating the game over popup. Additionally, TimerText invokes Timer's getter method GetTimeLeft() in Update() to appropriately update the timer text with the remaining time every frame.

## Open-Source assets
- [Cat fighter spritesheet](https://opengameart.org/content/cat-fighter-sprite-sheet)
- [Food sprites](https://rcpstd.itch.io/pixel-food-pack)