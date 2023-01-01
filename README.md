# Gazyi.ATMinions
Northstar mod that gives NPC grunts and spectres custom weapons and anti-titan capabilities.

### Server ConVars
##### Weapon distribution
```
sv_npc_give_random_primary (Default value: 1) - Allow NPCs spawn with random primary weapon.
sv_npc_give_antititan (Default value: 1) - Allow NPCs spawn with anti-titan weapon.
sv_npc_give_random_grenades (Default value: 1) - Allow NPCs spawn with random grenades.
sv_npc_allow_custom_ai_random_weapon (Default value: 0) - Allow overriding weapons for NPCs with non-default AI settings.
sv_npc_allow_random_grenades_no_default (Default value: 0) - Allow NPCs spawn with random grenades when they don't have any grenade set in AI settings.
```
##### Weapon lists 
Those cvars overwrite gamemode script lists. They won't work if `aitdm_archer_grunts` ConVar is enabled.

Example: `sv_npc_grunt_weapons mp_weapon_rspn101,mp_weapon_dmr,mp_weapon_r97,mp_weapon_lmg`
```
sv_npc_grunt_weapons - List of weapons that grunts will use.
sv_npc_spectre_weapons - List of weapons that spectres will use.
sv_npc_antititan_weapons - List of anti-titan weapons that NPCs will use.
sv_npc_grenades - List of grenades that NPCs will use.
```
##### AI and spawn ConVars
```
sv_npc_allow_switch_weapons (Default value: 1) - Allow NPCs switch weapons.
sv_npc_antititan_assign_rate (Default value: 4) - Every 4th NPC will get an anti-titan weapon on spawn.
```
### Known issues
- Changing weapon list ConVars back to empty string will restore it to base default weapon list (NPCs will spawn only with R-101/Archer/Frag Grenades).
- Server crash when NPC is using Smart Pistol.
- Client crash if Thunderbolt projectile spawned by dead NPC hit player titan.
- NPCs equipped with Cold War can't shoot.
- Most of ordnance weapons don't activate if they're thrown by NPCs.
