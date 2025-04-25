---
generator: doxide
---


# MaitrePokemon

**class MaitrePokemon: public AEntrainer**

@brief Represents a Master Trainer with boosted attack damage.


## Functions

| Name | Description |
| ---- | ----------- |
| [MaitrePokemon](#MaitrePokemon) | @brief Constructs a Master Trainer with name and six Pokémon. |
| [getPokemonAttackDamage](#getPokemonAttackDamage) | @brief Gets boosted attack damage (125% of base), or 0 if fainted. |
| [interact](#interact) | @brief Custom dramatic interaction for master trainers. |

## Function Details

### MaitrePokemon<a name="MaitrePokemon"></a>
!!! function "MaitrePokemon(const std::string&amp;, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon)"

    @brief Constructs a Master Trainer with name and six Pokémon.
    
    :material-location-enter: `name`
    :       Master trainer’s name.
    
    :material-location-enter: `p1..p6`
    :     Six Pokémon for the master’s team.
    

### getPokemonAttackDamage<a name="getPokemonAttackDamage"></a>
!!! function "int getPokemonAttackDamage(std::size_t) override"

    @brief Gets boosted attack damage (125% of base), or 0 if fainted.
    
    :material-location-enter: `index`
    :    Zero-based position of the Pokémon.
    
    :material-keyboard-return: **Return**
    :    Boosted damage value, or 0 if HP indicates fainted.
    

### interact<a name="interact"></a>
!!! function "void interact() const override"

    @brief Custom dramatic interaction for master trainers.
    

