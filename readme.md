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
       +spell_damage in percent
       +elemental_damage in percent
       +area_damage in percent
       +damage_over_time in percent
       +gem_burning_damage in percent
    )
    * more_multiplicators (
        shock_stacks * 30%
       +vulnerability in percent
       +gem_rf_spelldamage in percent
       +gem_rf_quality_spelldamage in percent
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

Is there anything that needs to be done? Open an Issue or PR!