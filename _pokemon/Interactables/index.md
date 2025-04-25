---
generator: doxide
---


# Interactables



## Types

| Name | Description |
| ---- | ----------- |
| [AEntrainer](AEntrainer.md) | Maximum Team Size Current number  of Pokemon in team @brief Adds a Pokemon to the trainer's team :material-location-enter: `pokemon` :    The pokemon to add :material-keyboard-return: **Return** :    True if the Pokemon was successfully added (team not full) false otherwise @brief Removes a Pokemon from the trainer's team by it's index :material-location-enter: `index` :    Zero-based position of the Pokemon to remove :material-keyboard-return: **Return** :    True if removal succeeded, false otherwise @brief Retrieves a Pokemon from the team by its index :material-location-enter: `index` :    Zero-based position of the Pokemon to return :material-keyboard-return: **Return** :     A copy of the Pokemon at the given index @brief Gets the attack damage of a team mem :material-location-enter: `` : :material-keyboard-return: **Return** : @brief Abstract base trainer providing common implementation of IEntrainer. Manages a team of up to six Pokémon, offers default add/remove, battle logic, and stream output. Concrete trainers should override interaction behavior and may specialize attack damage.  |
| [AInteragir](AInteragir.md) | @brief Performs the interaction behavior. |
| [IEntrainer](IEntrainer.md) | @brief Interface for a Pokemon Trainer capable of managing a team of Pokemon Defines the basic operations for naming the trainer and adding, removing, retrieving POkemon and querying their attack damage  |
| [Interagir](Interagir.md) | @brief Interface for any interactable entity. |
| [Joueur](Joueur.md) | @brief Represents the player, tracking badges and battle record. |
| [LeaderDeGym](LeaderDeGym.md) | @brief Represents a Gym Leader who awards a badge upon defeat. |
| [MaitrePokemon](MaitrePokemon.md) | @brief Represents a Master Trainer with boosted attack damage. |
| [Pokemon](Pokemon.md) | @brief Represents a Pokémon with attributes such as name, types, HP, and attack. |

## Variables

| Name | Description |
| ---- | ----------- |
| [cities](#cities) | @brief Custom interaction monologue for the Master Trainer upon battle. |
| [fightOver](#fightOver) | @brief Adds a Pokémon to this trainer’s team if there is available space. |
| [isLeader](#isLeader) | @brief Constructs a Gym Leader with a name, gym name, badge, and six Pokémon. |
| [nickname](#nickname) | @brief Gets the Pokémon’s name. |
| [pokemon](#pokemon) | @brief Gets the attack damage of the Pokémon at the given index, or 0 if the Pokémon is fainted. |
| [pokemon](#pokemon) | @brief Records a defeat against another trainer. |
| [typeAttcker1](#typeAttcker1) | @brief Default constructs a Pokémon with placeholder values. |

## Operators

| Name | Description |
| ---- | ----------- |
| [operator<<](#operator_u003c_u003c) | @brief Restores the Pokémon’s HP to its maximum value. |
| [operator<<](#operator_u003c_u003c) | @brief Swaps two Pokémon in the team by their indices. |

## Variable Details

### cities<a name="cities"></a>

!!! variable "std::vector&lt;std::string&gt; cities"

    @brief Custom interaction monologue for the Master Trainer upon battle.
               Chooses a random city and displays a dramatic ASCII-art defeat sequence.
    

### fightOver<a name="fightOver"></a>

!!! variable "bool fightOver"

    @brief Adds a Pokémon to this trainer’s team if there is available space.
    
    :material-location-enter: `pokemon`
    :    The Pokémon instance to add to the team.
    
    :material-keyboard-return: **Return**
    :    True if the Pokémon was successfully added; false if the team is already at maximum capacity.
    @brief Removes a Pokémon from this trainer’s team by its index.
    
    :material-location-enter: `index`
    :    Zero-based position of the Pokémon to remove.
    
    :material-keyboard-return: **Return**
    :    True if the Pokémon was successfully removed; false if the index is invalid or out of range.
    @brief Retrieves a reference to the Pokémon at the specified index in the trainer’s team.
    
    :material-location-enter: `index`
    :    Zero-based position of the Pokémon to retrieve.
    
    :material-keyboard-return: **Return**
    :    Reference to the Pokémon at the given index. Behavior is undefined if the index is out of range.
    @brief Returns all Pokémon currently on this trainer’s team.
    
    :material-keyboard-return: **Return**
    :    Const reference to the vector containing all team Pokémon.
    @brief Initiates and runs a turn-based battle against another trainer,
               displaying announcements, alternating attacks, and removing KIA Pokémon.
    
    :material-location-enter: `other`
    :    The opposing trainer to fight against.
    
    :material-keyboard-return: **Return**
    :    True if this trainer wins the battle (has more surviving Pokémon at the end),
                false if the opponent wins.
    

### isLeader<a name="isLeader"></a>

!!! variable "const LeaderDeGym&#42; isLeader"

    @brief Constructs a Gym Leader with a name, gym name, badge, and six Pokémon.
    
    :material-location-enter: `name`
    :      The leader’s name.
    
    :material-location-enter: `gymnase`
    :    The name of the gym they oversee.
    
    :material-location-enter: `badge`
    :     The badge awarded when defeated.
    
    :material-location-enter: `p1..p6`
    :    Six Pokémon to form the leader’s team.
    @brief Gets the badge name awarded by this Gym Leader.
    
    :material-keyboard-return: **Return**
    :    Const reference to the badge string.
    @brief Gets the name of the gym this leader oversees.
    
    :material-keyboard-return: **Return**
    :    Const reference to the gym name string.
    @brief Checks whether this Gym Leader has been beaten.
    
    :material-keyboard-return: **Return**
    :    True if the leader has been marked as beaten.
    @brief Marks this Gym Leader as beaten (badge can be claimed).
    @brief Custom interaction when the player defeats the Gym Leader.
               Displays a defeat monologue and awards the badge.
    @brief Constructs a Player with a name and six starting Pokémon.
    
    :material-location-enter: `name`
    :    The player’s name.
    
    :material-location-enter: `p1..p6`
    :    Six Pokémon to form the player’s initial team.
    @brief Records a victory against another trainer and collects their badge if they are a Gym Leader.
    
    :material-location-enter: `enemy`
    :    The trainer who was defeated.
    

### nickname<a name="nickname"></a>

!!! variable "const std::string&amp; nickname"

    @brief Gets the Pokémon’s name.
    
    :material-keyboard-return: **Return**
    :    Const reference to the name string.
    @brief Gets the Pokémon’s primary type.
    
    :material-keyboard-return: **Return**
    :    The primary elemental type.
    @brief Gets the Pokémon’s secondary type.
    
    :material-keyboard-return: **Return**
    :    The secondary elemental type.
    @brief Gets the current hit points of the Pokémon.
    
    :material-keyboard-return: **Return**
    :    The current HP value.
    @brief Gets the Pokémon’s attack move name.
    
    :material-keyboard-return: **Return**
    :    Const reference to the attack name.
    @brief Gets the base damage value of the Pokémon’s attack.
    
    :material-keyboard-return: **Return**
    :    The attack damage integer.
    @brief Checks if the Pokémon is still alive.
    
    :material-keyboard-return: **Return**
    :    True if hp > 0, false otherwise.
    @brief Sets the Pokémon’s current hit points.
    
    :material-location-enter: `hp`
    :     New HP value to assign.
    @brief Interacts with the Pokémon, printing a catchphrase or petting message.
    
    Special-cases Pikachu to say “Pika, pika !” and comments if HP is low.
    

### pokemon<a name="pokemon"></a>

!!! variable "Interactables::Pokemon&amp; pokemon"

    @brief Gets the attack damage of the Pokémon at the given index, or 0 if the Pokémon is fainted.
    
    :material-location-enter: `index`
    :    Zero-based index of the Pokémon whose attack damage to query.
    
    :material-keyboard-return: **Return**
    :    The attack damage value, or 0 if the Pokémon’s HP is -1 (indicating it cannot fight).
    

### pokemon<a name="pokemon"></a>

!!! variable "Interactables::Pokemon&amp; pokemon"

    @brief Records a defeat against another trainer.
    
    :material-location-enter: `enemy`
    :    The trainer who defeated this player.
    @brief Gets the list of badges the player has earned.
    
    :material-keyboard-return: **Return**
    :    Const reference to the vector of badge names.
    @brief Gets the number of fights the player has won.
    
    :material-keyboard-return: **Return**
    :    Number of victories.
    @brief Gets the number of fights the player has lost.
    
    :material-keyboard-return: **Return**
    :    Number of defeats.
    @brief Constructs a Master Trainer with a name and six powerful Pokémon.
    
    :material-location-enter: `name`
    :    The master trainer’s name.
    
    :material-location-enter: `p1..p6`
    :    Six Pokémon to form the master’s team.
    @brief Calculates a boosted attack damage (125% of base) for master trainers.
    
    :material-location-enter: `index`
    :    Zero-based index of the Pokémon whose attack to boost.
    
    :material-keyboard-return: **Return**
    :    The boosted attack damage, or 0 if Pokémon is fainted.
    

### typeAttcker1<a name="typeAttcker1"></a>

!!! variable "Pokemons::Type typeAttcker1"

    @brief Default constructs a Pokémon with placeholder values.
    
    Initializes name to "Undefined", types to Normal, HP to -1 (undefined),
    attack to "Undefined", and damage to 0.
    @brief Constructs a Pokémon with the specified attributes.
    
    :material-location-enter: `name`
    :              The Pokémon’s name.
    
    :material-location-enter: `type1`
    :             Primary elemental type.
    
    :material-location-enter: `type2`
    :             Secondary elemental type.
    
    :material-location-enter: `hp`
    :                Initial and maximum hit points.
    
    :material-location-enter: `attack`
    :            Name of the attack move.
    
    :material-location-enter: `attackDamages`
    :     Base damage value of the attack move.
    @brief Applies damage to this Pokémon based on type effectiveness.
    
    :material-location-enter: `baseDamage`
    :     The base damage of the incoming attack.
    
    :material-location-enter: `attacker`
    :       The attacking Pokémon to determine type multipliers.
    
    Prints a message indicating effectiveness, adjusts this.hp accordingly.
    

## Operator Details

### operator<<<a name="operator_u003c_u003c"></a>

!!! function "std::ostream&amp; operator&lt;&lt;(std::ostream&amp; os, const Pokemon&amp; obj)"

    @brief Restores the Pokémon’s HP to its maximum value.
    @brief Serializes the Pokémon’s details to an output stream.
    
    :material-location-enter: `os`
    :      The output stream to write to.
    
    :material-location-enter: `obj`
    :     The Pokémon instance to serialize.
    
    :material-keyboard-return: **Return**
    :    Reference to the output stream for chaining.
    

!!! function "std::ostream&amp; operator&lt;&lt;(std::ostream&amp; os, const AEntrainer&amp; obj)"

    @brief Swaps two Pokémon in the team by their indices.
    
    :material-location-enter: `ia`
    :    Index of the first Pokémon.
    
    :material-location-enter: `ib`
    :    Index of the second Pokémon.
    
    :material-keyboard-return: **Return**
    :    True if the swap succeeded (indices in range or ia == ib), false otherwise.
    @brief Default interaction behavior for an abstract trainer.
               Derived classes may override to provide custom dialogue or actions.
    @brief Serializes the trainer’s details and team to an output stream.
    
    :material-location-enter: `os`
    :    Output stream to write to.
    
    :material-location-enter: `obj`
    :    The trainer object to serialize.
    
    :material-keyboard-return: **Return**
    :    Reference to the output stream.
    

