# Dishonored Mission Stats without 3rd-party mods

The mission stats could be reviewed at any time, but you need to enable UDK Console first.

Add the following line:

```
m_PCBindings=(Name="Tilde",Command="set Console ConsoleKey Tilde | set PlayerController CheatClass class'DishonoredCheatManager' | EnableCheats")
```

to the "Engine.PlayerInput" section of the file:

```
%USERPROFILE%\My Documents\My Games\Dishonored\DishonoredGame\Config\DishonoredEngine.ini 
```

Now you can access Console by pressing tilde (~ / `) button.

---

The full list of console commands is published [here](https://docs.unrealengine.com/udk/Three/ConsoleCommands.html).

You need just the following:

```
GetAll DishonoredPlayerPawn m_MissionStatValues
```

The stats are printed in the same order as you see them on the "mission complete" screen.

Here is an example:

```
0: (m_Stat=28)                                      -- 
1: (m_Stat=30)                                      -- 
2: (m_Stat=3)                                       -- 
3: (m_Stat=4)                                       -- 
4: (m_Stat=10)                                      -- 0 : ghost
5: (m_Stat=34,m_fValue=5.000000,m_MaxValue=5)       -- runes
6: (m_Stat=35,m_fValue=8.000000,m_MaxValue=8)       -- bonecharms
7: (m_Stat=36,m_fValue=1.000000,m_MaxValue=1)       -- paintings
8: (m_Stat=37,m_fValue=3.000000,m_MaxValue=3)       -- 
9: (m_Stat=33,m_fValue=3758.000000,m_MaxValue=5635) -- coins
```
