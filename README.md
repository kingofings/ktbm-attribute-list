# `Attributes for Nosoops Framework:`

### `gain crit type on headshot` `(deprecated)`
- A weapon with this attribute will gain a set CritType for x amount of seconds.
- Attribute has the following varstrings:
	- `gain_amount` determins the amount of seconds gained e.g. 2.0
	- `max_amount` max time that can be stacked e.g 10.0
	- `crit_type` What CritType should be used when it is active: 1 for Mini-Crits, 2 for full Crits.
- Applicable to damage dealing weapons. (cannot be used on 2 weapons on the same loadout!!! (for now!))

### `mod crit type on reflect` `(deprecated)`
- A weapon that has this attribute will have the specified crit type applied on reflecting projectiles.
- Attribute has the following varstring:
	- `crit_type` What CritType should be used when it is active: 1 for Mini-Crits, 2 for full Crits (if set below 2 already critical projectiles will still crit or headshot(huntsman)).
- Applicable to Flamethrowers

### `mmmph rage gain on damage`
- A flamethrower with this attribute will cause rage to be gained from all damagetypes
- Attribute value is additive:
	- `0 = disabled`, `1 = enabled`
- Applicable to Flamethrowers

### ~~`custom sniperrifle props`~~ unused
- Changes the core behavior of sniper rifles.
- Attribute has the following varstrings:
	- `dmg_headshot` Float value, default 150.0
	- `dmg_bodyshot` Float value, default 50.0
	- `health_lethal_headshot` Int value, defines the amount of base health of a target which makes headshots always lethal. default 150.0
	- `drain_overheal` Bool, 1 = drain 0 = do nothing, this also disables `health_lethal_headshot`. default 1
- Applicable to Sniperrifles

### `mod backstab health absorb` `(deprecated)`
- Allows for changing bounds of the native `sanguisuge` attribute (It is adviced to disable the sanguisuge attribute so it does not interfere).
- Attribute has the following varstrings:
	- `min_gain` Int Value, Minimum Health gain on a backstab if victim has less than this amount of health, default 70
	- `max_overheal` Int Value, Max overheal that can be gained from backstabs, default 210
- Applicable to Knives

# `Attributes injected into Item Schema:`

## ~~`On Kill reload Secondary clip`~~ unused
### `ID: 10001`
- Value is additive

## `Crit type vs blast jumping players`
### `ID: 10002`
- This attribute only considers this against players who trigger TFCond_BlastJumping by themselves!
- The following values are valid:
	- -1 Remove any critType
	- 1 Deal Minicrits
	- 2 Deal Full Crits
- Value is additive
	
## `Damage Penalty vs players on ground`
### `ID: 10003`
- Value is percentage

## `Crit type vs airblasted players`
### `ID: 10004`
- The following values are valid:
	- -1 Remove any critType
	- 1 Deal Minicrits
	- 2 Deal Full Crits
- Value is addititve

## `On Kill reload x% of Secondary clip.`
### `ID: 10005`
- Value is percentage

## `Falloff Amount`
### `ID: 10006`
- ### Requires Falloff Divisor!
- Set the falloff amount eg. 50% = 50.0
- Value is additive

## `Falloff Divisor`
### `ID: 10007`
- ### Requires Falloff Amount!
- Set the falloff divisor eg. 50% = 50.0
- Value is additive

## `Rampup Amount`
### `ID: 10008`
- ### Requires Rampup Divisor!
- Set the falloff amount eg. 150% = 150.0
- Value is additive

## `Rampup Divisor`
### `ID: 10009`
- ### Requires Rampup Amount!
- Set the falloff divisor eg. 150% = 150.0
- Value is additive

## `Custom Barrage mod`
### `ID: 10010`
- Amount is sideways angle deviation
- Applicable Rocketlaunchers using `auto_fires_full_clip`
- Value is additive

## `Speed boost on any kill`
### `ID: 10011`
- Amount in seconds
- Value is additive

## `Remove Speed boost on any kill holster`
### `ID: 10012`
- Value is additive

## `Move speed (Bow required)`
### `ID: 10013`
- Value is percentage

## `Max Primary ammo (Bow required)`
### `ID: 10014`
- Value is percentage

## ~~`Headshot cooldown`~~ unused
### `ID: 10015`
- Value is additive
- Applicable to hitscan

## `Alt fire activates Banner`
### `ID: 10016`
- Value is additive

## `Self damage from this weapon`
### `ID: 10017`
- Value is percentage

## ~~`flame density overhaul`~~ unused
### `ID: 10018`
- Amount is damage. Specifying negative damage will increase the damage based on afterburn duration.
- Value is addititve

## `Clip cannot be resupplied`
### `ID: 10019`
- This does not work on items like lunchboxes jars, etc.
- Value is addititve

## `Damage bonus vs sapped buildings`
### `ID: 10020`
- Value is percentage.

## `Minicrit charge strike`
### `ID: 10021`
- Value is addititve

## `Speedboost on hit teamate duration`
### `ID: 10022`
- Value is addititve

## `Speedboost on hit teamate cooldown`
### `ID: 10023`
- Value is addititve

## `Crit type on reflect.`
### `ID: 10024`
- The following values are valid:
	- -1 Remove any critType
	- 1 Deal Minicrits
	- 2 Deal Full Crits
- Value is addititve
- Applicable to Flamethrowers
	
## `Kill refills Meter non melee`
### `ID: 10025`
- Value is percentage.

## `Lunchbox overheal prevention`
### `ID: 10026`
- Value is addititve

## `Damage Vulnerability while cloaked`
### `ID: 10027`
- Value is percentage

## `Set Projectile Speed`
### `ID: 10028`
- Value is speed in HU/s

## `Set Projectile Gravity`
### `ID: 10029`
- Value is addititve

## `Take damage on shot`
### `ID: 10030`
- Value is additive

## `Gain health on hit teammate crossbow`
### `ID: 10031`
- Value is additive

## `Jarate Rounds on kill`
### `ID: 10032`
- Value is additive
- Applicable to hitscan

## `Speed boost on any critical kill`
### `ID: 10033`
- Value is addititve

## ~~`Cow mangler charge for SC`~~ unused
### `ID: 10034`
- Value is additive
- Applicable to Short Circuit

## `Organs heal on hit teammate`
### `ID: 10035`
- Value is additive
- Applicable to melee weapons with organ attribute.

## `Melee death causes jarate explosion`
### `ID: 10036`
- Value is additive

## `Ignore no headshots uncharged while scoped`
### `ID: 10037`
- Value is additive, includes 0.2 Quickscope cooldown makes classic work like normal sniper rifle slowdown while scoped.
- Applicable to Sniper Rifles.

## ~~`Permanent Health penalty on Holster`~~ unused
### `ID: 10038`
- Value is additive

## `Mark for death on holster exact`
### `ID: 10039`
- Value is additive

## `Soda Popper Hype is jump height`
### `ID: 10040`
- Value is percentage
- Applicable to Soda Popper.

## `Mult Falldamage`
### `ID: 10041`
- Value is inverted percentage

## `Self Marked enemies health minicrits on death`
### `ID: 10042`
- Value is percentage
- Value of -1.0: Healrate = damage.
- Duration ConVar: `ktbm_m4d_health_minicrits_cap`

## `effect bar recharge rate increased secondary`
### `ID: 10043`
- Value is inverted percentage

## `While Taunting: Heal yourself`
### `ID: 10044`
- Value is additive
- Value is healrate/s. Integers Only!

## `On Backstab: Knife Melts`
### `ID: 10045`
- Value is additive

## `On Rage: Ignite on Hit`
### `ID: 10046`
- Value is addititve
- Value is burn time
- Requires 10047 (Rage: Ignite on Hit Gain Amount")
- Rage Duration is ConVar (duration in seconds): `ktbm_fire_rage_duration`

## `Rage: Ignite on Hit Gain Amount`
### `ID: 10047`
- Value is addititve
- Value is rage gained per 1 damage.
- Requires 10046 (On Rage: Ignite on Hit)

## `Overwrite Revenge Crit Type`
### `ID: 10048`
- The following values are valid:
	- 1 Minicrits
- Value is addititve
- Applicable to revenge weapons
	
## ~~`Negative version of effectbar_recharge_rate`~~ unused in pvp
### `ID: 10049`
- Existing native attribute injected as "negative" effect. (For mvm)

## ~~`effect bar recharge rate isolated secondary`~~ unused in pvp
### `ID: 10050`
- Does not interfere with existing native attribute
- Value is inverted percentage

## `No Flaregun Afterburn`
### `ID: 10051`
- Value is addititve
- The following values are valid:
	- 1 No Afterburn on direct hit
	- 2 No Afterburn on explosive hit
- Applicable to Flareguns

## `Flaregun Crit type vs burning player on direct hit`
### `ID: 10052`
- Value is addititve
- The following values are valid:
	- 1 Minicrit
	- 2 Full Crits
- Applicable to Flareguns

## `Speed boost on headshot`
### `ID: 10053`
- Value is addititve
- Value is duration.
- Lethal hits multiplies duration by 2.
- Applicable to headshotting weapons.

## `Has amplifier`
### `ID: 10054`
- Value is addititve
- Does nothing only used for checking if player is using amplifier


## `Extinguish on hit`
### `ID: 10055`
- Value is addititve

## `Mult afterburn heal`
### `ID: 10056`
- Value is additive

## `Mult player movespeed while carrying flag`
### `ID: 10057`
- Value is percentage

## `Crit Type on any headshot`
### `ID: 10058`
- Value is addititve
- Value is CritType (1 MiniCrits, 2 Full Crits)
- Requires `10059 Crit Type on any headshot duration`

## `Crit Type on any headshot duration`
### `ID: 10059`
- Value is addititve
- Requires `10058 Crit Type on any headshot`

## `Crit Type on any headshot duration limit`
### `ID: 10060`
- Value is addititve
- Requires `10058 Crit Type on any headshot`

## `lunchbox mult throw velocity`
### `ID: 10061`
- Value is percentage

## `no move penalty while hauling`
### `ID: 10062`
- Value is additive

## `dmg vuln while hauling`
### `ID: 10063`
- Value is percentage

## `mult dmg ubercharge scale`
### `ID: 10064`
- Value is additive

## `mult damage vs tagged player`
### `ID: 10065`
- Value is percentage

## `universal upgrade cost`
### `ID: 10066`
- Value is additive

## `backattack flame minicrits dotproduct`
### `ID: 10067`
- Value is additive dot product

## `custom flame rampup`
### `ID: 10068`
- Value is additive time until rampup resets
- Ramp up scale controlled by ktbm_flame_rampup_scale

## ~~`projectile penetration negative`~~ unused in pvp
### `ID: 10069`
- Value is additive
- Injection of native attribute as negative variant for mvm

## `is bison`
### `ID: 10070`
- Value is additive
- Does nothing only used to check if player is using bison

## `revenge crit on crit kill`
### `ID: 10071`
- Value is additive

## `mult movespeed resource level delay`
### `ID: 10072`
- Value is percentage
- Delay controlled by : `ktbm_mult_movespeed_resource_delay`

## `remove speed boost unrev`
### `ID: 10073`
- Value is additive

## `debuff drain while active`
### `ID: 10074`
- Value is additive

## `crit type vs burning player club`
### `ID: 10075`
- Value is additive
- Value is CritType (1 MiniCrits, 2 Full Crits)

## `steak penalty`
### `ID: 10076`
- Value is additive

## `crit vuln while parachute blast dmg`
### `ID: 10077`
- Value is additive
- Value is CritType (1 MiniCrits, 2 Full Crits)

## `custom critical falloff`
### `ID: 10078`
- Value is additive

## `mult item meter damage`
### `ID: 10079`
- Value is percentage

## `wearable health break rifle`
### `ID: 10080`
- Value is percentage

## `wearable health break rifle movespeed`
### `ID: 10081`
- Value is percentage

## `flaregun blast jump state`
### `ID: 10082`
- Value is additive
