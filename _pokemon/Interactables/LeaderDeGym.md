---
generator: doxide
---


# LeaderDeGym

**class LeaderDeGym: public AEntrainer**

@brief Represents a Gym Leader who awards a badge upon defeat.


## Variables

| Name | Description |
| ---- | ----------- |
| [badge](#badge) |     Name of the badge awarded. |
| [gymnase](#gymnase) |     Gym name. |
| [beaten](#beaten) |     Whether the leader has been defeated. |

## Functions

| Name | Description |
| ---- | ----------- |
| [LeaderDeGym](#LeaderDeGym) | @brief Constructs a Gym Leader with name, gym, badge, and six Pokémon. |
| [getBadge](#getBadge) | @brief Gets the badge this leader awards. |
| [getGymnase](#getGymnase) | @brief Gets the name of this leader’s gym. |
| [wasBeaten](#wasBeaten) | @brief Checks if the leader has been beaten. |
| [getBeaten](#getBeaten) | @brief Marks the leader as beaten so the badge can be claimed. |
| [interact](#interact) | @brief Interaction behavior after being defeated. |

## Variable Details

### badge<a name="badge"></a>

!!! variable "std::string badge"

        Name of the badge awarded.
    

### beaten<a name="beaten"></a>

!!! variable "bool beaten"

        Whether the leader has been defeated.
    

### gymnase<a name="gymnase"></a>

!!! variable "std::string gymnase"

        Gym name.
    

## Function Details

### LeaderDeGym<a name="LeaderDeGym"></a>
!!! function "LeaderDeGym(const std::string&amp;, const std::string&amp;, const std::string&amp;, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon, Interactables::Pokemon)"

    @brief Constructs a Gym Leader with name, gym, badge, and six Pokémon.
    
    :material-location-enter: `name`
    :         Leader’s name.
    
    :material-location-enter: `gymnase`
    :      Name of the gym.
    
    :material-location-enter: `badge`
    :        Badge name awarded upon defeat.
    
    :material-location-enter: `p1..p6`
    :       Six Pokémon forming the leader’s team.
    

### getBadge<a name="getBadge"></a>
!!! function "const std::string&amp; getBadge() const"

    @brief Gets the badge this leader awards.
    
    :material-keyboard-return: **Return**
    :    Const reference to the badge name.
    

### getBeaten<a name="getBeaten"></a>
!!! function "void getBeaten()"

    @brief Marks the leader as beaten so the badge can be claimed.
    

### getGymnase<a name="getGymnase"></a>
!!! function "const std::string&amp; getGymnase() const"

    @brief Gets the name of this leader’s gym.
    
    :material-keyboard-return: **Return**
    :    Const reference to the gym name.
    

### interact<a name="interact"></a>
!!! function "void interact() const override"

    @brief Interaction behavior after being defeated.
    

### wasBeaten<a name="wasBeaten"></a>
!!! function "bool wasBeaten() const"

    @brief Checks if the leader has been beaten.
    
    :material-keyboard-return: **Return**
    :    True if beaten, false otherwise.
    

