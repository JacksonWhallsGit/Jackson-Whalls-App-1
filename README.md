# Jackson-Whalls-App-1
This is my completed John Lemon tutorial: https://learn.unity.com/project/john-lemon-s-haunted-jaunt-3d-beginner

For the changes, I added a "Cloak" ability to the player. When they press "E", the John Lemon character plays a small animation, and takes out his cloak. While the cloak is active, he cannot be seen by enemies. I could have done this by just creating a box collider on the object, but I thought that might introduce issues when getting too close to enemies (their raycasts may start inside the cloak, and then it would not function properly. So instead, I added code to the observer script to determine if John is wearing the cloak or not - if he is, they will not fire rays to detect the player until he is uncloaked.

There is also a cooldown timer at the bottom of the screen. It is in a transparent yellow box with a background image of John with his cloak on. This tells you when you can and cannot cloak. When the timer is counting down, it means the ability is on cooldown, and you cannot use it until it once again says "Cloak".

To create the animation, I took the John_Idle animation, copied it into blender, changed the keyframes into the desired poses, and exported the new fbx.

The script for the cloak is located under _scripts -> CloakPlayer.cs
The script for the timer is located under _scripts -> UICloakTimer.cs
The animation is located under Animation -> Animation -> John@Cloak. (You will also see I was playing around with an animation for cloaking while walking, but it was a bit time-consuming since I've never used blender or made 3D unity animations, so I decided to not implement it).
