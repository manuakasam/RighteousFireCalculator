Path of Exile, Righteous Fire Calculator
========================================

This is a very simple calculator to get the damage values for your righteous fire. It uses this formula:

```
    (
        player_health * 0.5
       +player_shield * 0.5
    )
    * damage_multiplicators (
        global_damage_increase in percent
       +burning_damage in percent
       +fire_damage in percent
       +spell_damage in percent (to be implemented)
       +elemental_damage in percent
       +area_damage in percent
       +damage_over_time in percent
       +gem_burning_damage in percent
    )
    * more_multiplicators (
        shock_stacks * 30%
       +vulnerability in percent
       +moce_spelldamage in percent (to be implemented)
    )
    * mob_resistances - curses_multiplicators (
        flamability
       +elemental_weakness
       +elemental_weakness_quality
       +elemental_equilibrium
    )
```


Contributing and TODO
=====================

Following things need to be done:

- implement spelldamage
- implement more spelldamage