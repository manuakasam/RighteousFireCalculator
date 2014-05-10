Path of Exile, Righteous Fire Calculator
========================================

This is a very simple calculator to get the damage values for your righteous fire. It uses this formula:

```
(                                       // Righteous Fire Base Value
    ( player_attr.hp / 2 )              // 50% of Player Hitpoints
  + ( player_attr.es / 2 )              // 50% of Player Energy Shield
)
* ( 1 + (                               // Additive Damage multipliers
    (
        player_attr.gic                 // Global Damage Increase
      + player_attr.bd                  // Burning Damage Talents + Gear
      + player_attr.fd                  // Fire Damage Talents + Gear
      + player_attr.ad                  // Area Damage Talents + Gear
      + player_attr.dot                 // Damage over Time modifiers
      + gem_bd_selected                 // Burning Damage Gem
    ) / 100
) )
* ( 1 + (                               // Additive MORE Damage multipliers
    (
        gem_ce_selected                 // Concentrated Effect Gem
      + ( curse_v * curse_v_value )     // Vulnerability Curse
    ) / 100
) )
* ( 1 + (                               // Mob Resistance Multipliers
    (
        curse_f_selected                // Flamability Curse
      + curse_ew_selected               // Elemental Weakness Curse
      + curse_ew_quality_selected       // Elemental Weakness Quality
      + ( curse_ee * curse_ee_value )   // Elemental Equilibrium
    ) / 100
) )
```

This formula is pretty accurate except for the calculations of the mob resistance multipliers. Values there are nothing
but a theoretic model of the damage that we do. Mobs Resist Damage and just because we bypass damage it doesn't mean
that we do more Damage as Base-Value. It is useful for finding out which Curse is effective or not though.


Contributing and TODO
=====================

Following things need to be done:

- Add option for Base-Resistances of Mobs (+-75/50/25/0)
- Properly calculate Damage against Mob-Reistances
- Properly calculate Damage using Curses
- Add Leer-Casts Aura