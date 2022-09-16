Features:

- Press a configured key (` by default) to quickly stack items from your inventory into a currently opened or nearby containers.

- Alt+Click an item in inventory to exclude it from automatic stacking.

- Alt+Right Click an item in inventory to exclude that item from automatic stacking (item tooltip will change).

Configuration:
After you first run your game with the mod enabled, a config file will appear at .../Valheim/BepInEx/config/org.bepinex.plugins.valheim.quick_stack.cfg
You can customize the values to best suit your needs:
[QuickStack]

\#\# Get key codes here: https://docs.unity3d.com/ScriptReference/KeyCode.html
\# Setting type: String
\# Default value: BackQuote
QuickStackKey = BackQuote

\#\# How far from you is nearby, greater value = greater range
\# Setting type: Single
\# Default value: 3
NearbyRange = 3

\#\# Whether to completely exclude consumables from quick stacking (food, potions).
\# Setting type: Boolean
\# Default value: true
IgnoreConsumable = true

\#\# Whether to completely exclude ammo from quick stacking (arrows)
\# Setting type: Boolean
\# Default value: true
IgnoreAmmo = true

\#\# Whether to put all types of trophies in the container if any trophy is found in that container.
\# Setting type: Boolean
\# Default value: true
CoalesceTrophies = true