---
generator: doxide
---


# Joueur

**class Joueur: public AEntrainer**

@brief Represents the player, tracking badges and battle record.


## Variables

| Name | Description |
| ---- | ----------- |
| [badges](#badges) |     Earned badge names. |

## Functions

| Name | Description |
| ---- | ----------- |
| [Joueur](#Joueur) | @brief Constructs a player with name and six starting Pokémon. |
| [winFight](#winFight) | @brief Records a win and collects a badge if opponent is a Gym Leader. |
| [loseFight](#loseFight) | @brief Records a loss against another trainer. |
| [getBadges](#getBadges) | @brief Gets the list of badges the player has. |
| [getWonFights](#getWonFights) | @brief Gets the number of fights won. |
| [getLostFights](#getLostFights) | @brief Gets the number of fights lost. |

## Variable Details

### badges<a name="badges"></a>

!!! variable "std::vector&lt;std::string&gt; badges"

        Earned badge names.
        Number of wins.
        Number of losses.
    

## Function Details

### Joueur<a name="Joueur"></a>
!!! function "Joueur(const std::string&amp;, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon)"

    @brief Constructs a player with name and six starting Pokémon.
    
    :material-location-enter: `name`
    :       Player’s name.
    
    :material-location-enter: `p1..p6`
    :     Six Pokémon for the initial team.
    

### getBadges<a name="getBadges"></a>
!!! function "const std::vector&lt;std::string&gt;&amp; getBadges() const"

    @brief Gets the list of badges the player has.
    
    :material-keyboard-return: **Return**
    :    Const reference to the badge vector.
    

### getLostFights<a name="getLostFights"></a>
!!! function "std::size_t getLostFights() const"

    @brief Gets the number of fights lost.
    
    :material-keyboard-return: **Return**
    :    Loss count.
    

### getWonFights<a name="getWonFights"></a>
!!! function "std::size_t getWonFights() const"

    @brief Gets the number of fights won.
    
    :material-keyboard-return: **Return**
    :    Win count.
    

### loseFight<a name="loseFight"></a>
!!! function "void loseFight(const AEntrainer&amp;)"

    @brief Records a loss against another trainer.
    
    :material-location-enter: `enemy`
    :    The trainer who won.
    

### winFight<a name="winFight"></a>
!!! function "void winFight(const AEntrainer&amp;)"

    @brief Records a win and collects a badge if opponent is a Gym Leader.
    
    :material-location-enter: `enemy`
    :    The defeated trainer.
    

