---
generator: doxide
---


# Pokemons



## Types

| Name | Description |
| ---- | ----------- |
| [Type](Type.md) | @brief Enumeration of all possible Pokémon elemental types. |

## Variables

| Name | Description |
| ---- | ----------- |
| [lowerType](#lowerType) | @brief Copy constructor for the Type wrapper. |

## Operators

| Name | Description |
| ---- | ----------- |
| [operator<<](#operator_u003c_u003c) | @brief Retrieves the underlying raw enum value. |

## Variable Details

### lowerType<a name="lowerType"></a>

!!! variable "std::string lowerType"

    @brief Copy constructor for the Type wrapper.
    
    :material-location-enter: `other`
    :    The Type instance to copy from.
    @brief Constructs a Type from a raw enum value.
    
    :material-location-enter: `other`
    :    The raw _Type enum value.
    @brief Constructs a Type by parsing its name.
    
    :material-location-enter: `__type`
    :    Case-insensitive string representing the type name,
               e.g. "Feu", "eau", "PLANTE".
    
    !!! note
     If the provided string does not match any known type, _type
                  will remain uninitialized (consider handling unknown cases).
    

## Operator Details

### operator<<<a name="operator_u003c_u003c"></a>

!!! function "std::ostream&amp; operator&lt;&lt;(std::ostream&amp; os, const Type&amp; obj)"

    @brief Retrieves the underlying raw enum value.
    
    :material-keyboard-return: **Return**
    :    The raw Type::_Type held by this wrapper.
    @brief Inserts the Type’s name into an output stream.
    
    :material-location-enter: `os`
    :     The stream to write to.
    
    :material-location-enter: `obj`
    :    The Type instance whose name will be printed.
    
    :material-keyboard-return: **Return**
    :    Reference to the output stream.
    

