---
generator: doxide
---


# Pokemon

**class Pokemon: public Interactables::AInteragir**

@brief Represents a Pokémon with attributes such as name, types, HP, and attack.


## Variables

| Name | Description |
| ---- | ----------- |
| [type1](#type1) | The Pokemon's name  |
| [type2](#type2) | Primary Type  |
| [max_hp](#max_hp) | Secondary Type (Type 2 is None if no Type2)  |
| [hp](#hp) | Current HealthPoints  |
| [attack](#attack) | Current HealthPoints  |
| [attackDamages](#attackDamages) | Name of the attack move  |

## Operators

| Name | Description |
| ---- | ----------- |
| [operator<<](#operator_u003c_u003c) | @brief Outputs the Pokémon’s details to a stream. |

## Functions

| Name | Description |
| ---- | ----------- |
| [Pokemon](#Pokemon) | Damage Value of the attack @brief Default constructor initializes a Pokémon with placeholder values. |
| [Pokemon](#Pokemon) | @brief Constructs a Pokémon with specific attributes. |
| [recevoirDegats](#recevoirDegats) | @brief Applies damage to this Pokémon, reducing its HP according to type effectiveness. |
| [getName](#getName) | @brief Gets the Pokémon’s name. |
| [getType1](#getType1) | @brief Gets the Pokémon’s primary type. |
| [getType2](#getType2) | @brief Gets the Pokémon’s secondary type. |
| [getHP](#getHP) | @brief Gets the current HP of the Pokémon. |
| [getAttack](#getAttack) | @brief Gets the name of the Pokémon’s attack move. |
| [getAttackDamages](#getAttackDamages) | @brief Gets the damage value of the Pokémon’s attack. |
| [isAlive](#isAlive) | @brief Checks if the Pokémon is still alive. |
| [setHP](#setHP) | @brief Sets the Pokémon’s current HP. |

## Variable Details

### attack<a name="attack"></a>

!!! variable "std::string attack"

    Current HealthPoints
    

### attackDamages<a name="attackDamages"></a>

!!! variable "int attackDamages"

    Name of the attack move
    

### hp<a name="hp"></a>

!!! variable "int hp"

    Current HealthPoints
    

### max_hp<a name="max_hp"></a>

!!! variable "int max_hp"

    Secondary Type (Type 2 is None if no Type2)
    

### type1<a name="type1"></a>

!!! variable "Pokemons::Type type1"

    The Pokemon's name
    

### type2<a name="type2"></a>

!!! variable "Pokemons::Type type2"

    Primary Type
    

## Operator Details

### operator<<<a name="operator_u003c_u003c"></a>

!!! function "std::ostream&amp; operator&lt;&lt;(std::ostream&amp;, const Pokemon&amp;)"

    @brief Outputs the Pokémon’s details to a stream.
    
    :material-location-enter: `os`
    :    The output stream.
    
    :material-location-enter: `pokemon`
    :    The Pokémon instance to serialize.
    
    :material-keyboard-return: **Return**
    :    A reference to the output stream.
    

## Function Details

### Pokemon<a name="Pokemon"></a>
!!! function "Pokemon()"

    Damage Value of the attack
    @brief Default constructor initializes a Pokémon with placeholder values.
    

!!! function "Pokemon(const std::string&amp;, Pokemons::Type, Pokemons::Type, int, const std::string&amp;, int)"

    @brief Constructs a Pokémon with specific attributes.
    
    :material-location-enter: `name`
    :    The name of the Pokémon.
    
    :material-location-enter: `type1`
    :    The primary type.
    
    :material-location-enter: `type2`
    :    The secondary type.
    
    :material-location-enter: `hp`
    :    Initial hit points.
    
    :material-location-enter: `attack`
    :    The name of the attack move.
    
    :material-location-enter: `attackDamages`
    :    The damage value of the attack.
    

### getAttack<a name="getAttack"></a>
!!! function "const std::string&amp; getAttack() const"

    @brief Gets the name of the Pokémon’s attack move.
    
    :material-keyboard-return: **Return**
    :    Reference to the attack name string.
    

### getAttackDamages<a name="getAttackDamages"></a>
!!! function "int getAttackDamages() const"

    @brief Gets the damage value of the Pokémon’s attack.
    
    :material-keyboard-return: **Return**
    :    The attack damage.
    

### getHP<a name="getHP"></a>
!!! function "int getHP() const"

    @brief Gets the current HP of the Pokémon.
    
    :material-keyboard-return: **Return**
    :    The HealthPoints.
    

### getName<a name="getName"></a>
!!! function "const std::string&amp; getName() const"

    @brief Gets the Pokémon’s name.
    
    :material-keyboard-return: **Return**
    :    Reference to the name string.
    

### getType1<a name="getType1"></a>
!!! function "Pokemons::Type getType1() const"

    @brief Gets the Pokémon’s primary type.
    
    :material-keyboard-return: **Return**
    :    The primary type.
    

### getType2<a name="getType2"></a>
!!! function "Pokemons::Type getType2() const"

    @brief Gets the Pokémon’s secondary type.
    
    :material-keyboard-return: **Return**
    :    The secondary type.
    

### isAlive<a name="isAlive"></a>
!!! function "bool isAlive() const"

    @brief Checks if the Pokémon is still alive.
    
    :material-keyboard-return: **Return**
    :    True if HP > 0, false otherwise.
    

### recevoirDegats<a name="recevoirDegats"></a>
!!! function "void recevoirDegats(int, const Pokemon&amp;)"

    @brief Applies damage to this Pokémon, reducing its HP according to type effectiveness.
    
    :material-location-enter: `damage`
    :    Base damage to apply.
    
    :material-location-enter: `attacker`
    :    The attacking Pokémon used to compute type multipliers.
    

### setHP<a name="setHP"></a>
!!! function "void setHP(int)"

    @brief Sets the Pokémon’s current HP.
    
    :material-location-enter: `newHP`
    :    The new hit points value.
    

