# Northstar - Gravity

## Preparation

In those "guide" called premade I will consider that you know how to proprely setup / start modding your game. If it's not your case you must read the "General info", refer to this [link](https://noskill.gitbook.io/titanfall2/how-to-start-modding/modding-introduction)

Any suggestion are welcome, you can submit your request / idea on NS Discord or even if you made your own premade weapon / set. You can reach me via [contact](https://noskill.gitbook.io/titanfall2/contact) details.

### Demo

{% embed url="https://www.youtube.com/watch?v=A2ke8bzzi30" %}

## Railgun

### Editing

To get this railgun, you will need to edit one text files. No specific software exept your text editor.

Go to this location

> englishclient\_mp\_common.bsp.pak000\_dir.vpk\scripts\weapons

Open the file `mp_titanweapon_sniper.txt` with your text editor.

Find and replace the following values in your file. **Note:** Do not copy paste this entire code block into your original file, replace string by string or you might resolve with a none working file.

Thoose value change the railgun projectile to a blue one for regular shot and to gravity vortex for the full charged shots.

```
"projectile_trail_effect_0"				"wpn_grenade_frag_blue"
"projectile_trail_effect_1"				"wpn_grenade_frag_blue"
"projectile_trail_effect_2"				"P_wpn_grenade_gravity"
```

Those values change the muzzle flash to an electric one. _note:_ muzzle flash apply when you shoot, this is not the vortex effect when you charge the railgun.

```
"fx_muzzle_flash_view"					"wpn_muzzleflash_arc_cannon_fp"
"fx_muzzle_flash_world"					"wpn_muzzleflash_arc_cannon_fp"
"fx_muzzle_flash_attach"				"muzzle_flash"
```

This list of value change the charge effect and sound of the railgun. I change the charge effect **and**sound to the gravity vortex.

```
"charge_sound_1p"					"weapon_gravitystar_preexplo"
"charge_full_sound_1p"					"Weapon_Titan_Sniper_SustainLoop"
"charge_effect_1p"					"P_wpn_grenade_gravity"
"charge_effect_3p"					"P_wpn_grenade_gravity"
```

### Crosshair

Here is the crosshair I'm using on the railgun

```
active_crosshair_count				"2"
rui_crosshair_index					"0"

RUI_CrosshairData
{
	DefaultArgs
	{
		adjustedSpread				weapon_spread
		adsFrac 					player_zoomFrac
		isSprinting					player_is_sprinting
		isReloading					weapon_is_reloading
		readyFrac                   progress_ready_to_fire_frac
		teamColor					crosshair_team_color
		isAmped						weapon_is_amped
		chargeFrac                  player_chargeFrac
		crosshairMovementX          crosshair_movement_x
		crosshairMovementY          crosshair_movement_y
	}

	Crosshair_1
	{
		"ui"						"ui/crosshair_charge_rifle"
		"base_spread"				"10.0"
		Args
		{
			isFiring				weapon_is_firing
		}
	}
	Crosshair_1
	{
		"ui"						"ui/crosshair_circle2_small"
		"base_spread"				"0.0"
		Args
		{
			isFiring				weapon_is_firing
		}
	}
}
```

## Flight core

### Editing

To get this flight core, you will need to edit one text files. No specific software exept your text editor.

For the first file you need to edit, go to this location

> englishclient\_mp\_common.bsp.pak000\_dir.vpk\scripts\vscripts\weapons

Open the file `mp_titanweapon_flightcore_rockets.txt` with your text editor.

Find and replace the following values in your file. **Note:** Do not copy paste this entire code block into your original file, replace string by string or you might resolve with a none working file.

This will change the muzzle flash to an electric one.

```
"fx_muzzle_flash_view"					"wpn_muzzleflash_arc_cannon_fp"
"fx_muzzle_flash_world"					"wpn_muzzleflash_arc_cannon_fp"
"fx_muzzle_flash_attach"				"muzzle_flash_2"

"fx_muzzle_flash2_view"					"wpn_muzzleflash_arc_cannon_fp"
"fx_muzzle_flash2_world"				"wpn_muzzleflash_arc_cannon_fp"
"fx_muzzle_flash2_attach"				"muzzle_flash"
```

Change the projectile to the EPG one and changeed the impact to the arc launcher one.

```
"impact_effect_table" 					"exp_arc_ball"
"projectile_trail_effect_0" 				"P_plasma_proj_LG_DLight"
```

Changed the core sound to a soft "energy" one (that point is purely personnal taste) only for first person.

```
"fire_sound_1_player_1p"			"ShoulderRocket_Homing_Fire_1P"
"fire_sound_1_player_3p"			"weapon_titan_flightcore_rocket_fire_3p"
"fire_sound_2"					"Weapon_bulletCasings.Bounce"
```

### Crosshair

```
active_crosshair_count				"1"
rui_crosshair_index					"0"

RUI_CrosshairData
{
	DefaultArgs
	{
		adjustedSpread				weapon_spread
		adsFrac 					player_zoomFrac
		isSprinting					player_is_sprinting
		isReloading					weapon_is_reloading
		teamColor					crosshair_team_color
		isAmped						weapon_is_amped
		crosshairMovementX          crosshair_movement_x
		crosshairMovementY          crosshair_movement_y
	}

	Crosshair_1
	{
		"ui"						"ui/crosshair_tracker_rockets"
		"base_spread"				"0.0"
		Args
		{
			isFiring				weapon_is_firing
		}
	}
}
```

## Cluster missile

To get this cluster missle, you will need to edit one text files. No specific software exept your text editor.

Go to this location

> englishclient\_mp\_common.bsp.pak000\_dir.vpk\scripts\weapons

Open the file `mp_titanweapon_dumbfire_rockets.txt` with your text editor.

Find and replace the following values in your file. **Note:** Do not copy paste this entire code block into your original file, replace string by string or you might resolve with a none working file.

This will change the cluster icon to the one from Frontier Defense. The cluster missile animation will change to the twin cluter tier mod from Frontier Defense.

```
"hud_icon"		"rui/menu/fd_menu/upgrade_northstar_twin_cluster_hud"
"viewmodel"		"models/weapons/titan_raptor_rocket_pod/atpov_titan_raptor_rocket_pod_core.mdl"
```

This change the cluster missile projectile to the gravity vortex, which is the theme of this Northstar theme.

```
"projectile_trail_effect_0"			"P_wpn_grenade_gravity"
```

## Tether trap

To get this tether trap effect, you will need to edit one text files. No specific software exept your text editor.

Go to this location

> englishclient\_mp\_common.bsp.pak000\_dir.vpk\scripts\weapons

Open the file `mp_titanability_tether_trap.txt` with your text editor.

Find and replace the following values in your file. **Note:** Do not copy paste this entire code block into your original file, replace string by string or you might resolve with a none working file.

This change the tether trap icon HUD to the one used in Frontier Defense.

```
"hud_icon"			"rui/menu/fd_menu/upgrade_northstar_explosive_trap_hud"
```

Those values make the tether trap this electric effect.

```
"impact_effect_table"				"P_wpn_arcTrap"
"projectile_trail_effect_0"			"P_wpn_arcball_trail_amp"
```
