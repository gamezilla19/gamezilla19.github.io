---
generator: doxide
---


# AInteragir

**class AInteragir : public Interagir**

@brief Performs the interaction behavior.
@brief Gets the name of the entity.

:material-keyboard-return: **Return**
:    Const reference to the name string.
@brief Virtual destructor.
@brief Default implementation of Interagir providing fallback behavior.


## Functions

| Name | Description |
| ---- | ----------- |
| [interact](#interact) | @brief Default constructor. |
| [getName](#getName) | @brief Retrieves the stored name. |

## Function Details

### getName<a name="getName"></a>
!!! function "const std::string&amp; getName() const override"

    @brief Retrieves the stored name.
    
    :material-keyboard-return: **Return**
    :    Const reference to the name string.
    

### interact<a name="interact"></a>
!!! function "void interact() const override"

    @brief Default constructor.
    @brief Fallback interaction when not overridden by derived class.
    
    :material-keyboard-return: **Return**
    :    Writes an error message to std::cerr.
    

