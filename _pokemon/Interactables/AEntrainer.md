---
generator: doxide
---


# AEntrainer

**class AEntrainer: public IEntrainer**

Maximum Team Size
Current number  of Pokemon in team
@brief Adds a Pokemon to the trainer's team

:material-location-enter: `pokemon`
:    The pokemon to add

:material-keyboard-return: **Return**
:    True if the Pokemon was successfully added (team not full) false otherwise
@brief Removes a Pokemon from the trainer's team by it's index

:material-location-enter: `index`
:    Zero-based position of the Pokemon to remove

:material-keyboard-return: **Return**
:    True if removal succeeded, false otherwise
@brief Retrieves a Pokemon from the team by its index

:material-location-enter: `index`
:    Zero-based position of the Pokemon to return

:material-keyboard-return: **Return**
:     A copy of the Pokemon at the given index
@brief Gets the attack damage of a team mem

:material-location-enter: ``
:

:material-keyboard-return: **Return**
:
@brief Abstract base trainer providing common implementation of IEntrainer.

Manages a team of up to six Pokémon, offers default add/remove,
battle logic, and stream output. Concrete trainers should override
interaction behavior and may specialize attack damage.


## Operators

| Name | Description |
| ---- | ----------- |
| [operator<<](#operator_u003c_u003c) | @brief Serializes trainer and team to an output stream. |

## Functions

| Name | Description |
| ---- | ----------- |
| [AEntrainer](#AEntrainer) | @brief Default constructor initializes an empty trainer. |
| [addPokemon](#addPokemon) | @brief Adds a Pokémon to the team if not full. |
| [rmPokemon](#rmPokemon) | @brief Removes a Pokémon from the team by index. |
| [getPokemon](#getPokemon) | @brief Retrieves a Pokémon by index. |
| [getAllPokemons](#getAllPokemons) | @brief Returns all Pokémon in the trainer’s team. |
| [fightAgainst](#fightAgainst) | @brief Executes a full battle sequence against another trainer. |
| [getPokemonAttackDamage](#getPokemonAttackDamage) | @brief Gets the attack damage of a Pokémon, or 0 if fainted. |
| [switchPokemons](#switchPokemons) | @brief Swaps two Pokémon in the team. |
| [interact](#interact) | @brief Default interaction stub; override for custom behavior.  |

## Operator Details

### operator<<<a name="operator_u003c_u003c"></a>

!!! function "std::ostream&amp; operator&lt;&lt;(std::ostream&amp;, const AEntrainer&amp;)"

    @brief Serializes trainer and team to an output stream.
    
    :material-location-enter: `os`
    :    Output stream.
    
    :material-location-enter: `obj`
    :    Trainer instance to serialize.
    
    :material-keyboard-return: **Return**
    :    Reference to the output stream.
    

## Function Details

### AEntrainer<a name="AEntrainer"></a>
!!! function "AEntrainer()"

    @brief Default constructor initializes an empty trainer.
    

### addPokemon<a name="addPokemon"></a>
!!! function "bool addPokemon(const Interactables::Pokemon&amp;) override"

    @brief Adds a Pokémon to the team if not full.
    
    :material-location-enter: `pokemon`
    :    The Pokémon to add.
    
    :material-keyboard-return: **Return**
    :    True on success, false if team is at max capacity.
    

### fightAgainst<a name="fightAgainst"></a>
!!! function "bool fightAgainst(IEntrainer&amp; other)"

    @brief Executes a full battle sequence against another trainer.
    
    :material-location-enter: `other`
    :    The opposing trainer.
    
    :material-keyboard-return: **Return**
    :    True if this trainer wins (more survivors), false otherwise.
    

### getAllPokemons<a name="getAllPokemons"></a>
!!! function "const std::vector&lt;Interactables::Pokemon&gt;&amp; getAllPokemons() const override"

    @brief Returns all Pokémon in the trainer’s team.
    
    :material-keyboard-return: **Return**
    :    Const reference to the vector of team Pokémon.
    

### getPokemon<a name="getPokemon"></a>
!!! function "Interactables::Pokemon&amp; getPokemon(std::size_t) override"

    @brief Retrieves a Pokémon by index.
    
    :material-location-enter: `index`
    :    Zero-based position of the Pokémon to retrieve.
    
    :material-keyboard-return: **Return**
    :    Reference to the Pokémon; undefined if index is invalid.
    

### getPokemonAttackDamage<a name="getPokemonAttackDamage"></a>
!!! function "int getPokemonAttackDamage(std::size_t) override"

    @brief Gets the attack damage of a Pokémon, or 0 if fainted.
    
    :material-location-enter: `index`
    :    Zero-based position of the Pokémon.
    
    :material-keyboard-return: **Return**
    :    Damage value, or 0 if the Pokémon’s HP indicates fainted.
    

### interact<a name="interact"></a>
!!! function "void interact() const override"

    @brief Default interaction stub; override for custom behavior.
    

### rmPokemon<a name="rmPokemon"></a>
!!! function "bool rmPokemon(std::size_t) override"

    @brief Removes a Pokémon from the team by index.
    
    :material-location-enter: `index`
    :    Zero-based position of the Pokémon to remove.
    
    :material-keyboard-return: **Return**
    :    True on success, false if index is invalid.
    

### switchPokemons<a name="switchPokemons"></a>
!!! function "bool switchPokemons(std::size_t, std::size_t)"

    @brief Swaps two Pokémon in the team.
    
    :material-location-enter: `ia`
    :    Index of the first Pokémon.
    
    :material-location-enter: `ib`
    :    Index of the second Pokémon.
    
    :material-keyboard-return: **Return**
    :    True if swap succeeded or indices equal; false if out of range.
    

