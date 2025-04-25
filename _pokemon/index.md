---
generator: doxide
---


# Projet Pokemon

Projet Pokemon Binome Hajdarevic Hugo et Tarlier Romain C++

:material-package: [Interactables](Interactables/index.md)
:   

:material-package: [Pokemons](Pokemons/index.md)
:   

## Types

| Name | Description |
| ---- | ----------- |
| [EntrainersFactory](EntrainersFactory.md) | @brief Factory class for loading different types of trainers from CSV files. |
| [PokemonFactory](PokemonFactory.md) | @brief Pokemon Factory is used as a class that is designed to avoid mistakes made by users  |
| [UI](UI.md) | @brief Controls global UI I/O actions. |

## Variables

| Name | Description |
| ---- | ----------- |
| [output](#output) | @brief Reads all players from a CSV file and constructs Joueur instances. |
| [output](#output) | @brief Reads all Gym Leaders from a CSV file and constructs LeaderDeGym instances. |
| [output](#output) | @brief Reads all Master Trainers from a CSV file and constructs MaitrePokemon instances. |
| [instance](#instance) | @brief Constructs the singleton Pokémon factory. |
| [m](#m) | @brief Retrieves a loaded Pokémon by its name. |
| [output](#output) | @brief Returns all Pokémon currently loaded in the factory. |

## Functions

| Name | Description |
| ---- | ----------- |
| [file](#file) | @brief Loads Pokémon definitions from a CSV file into the factory. |

## Variable Details

### instance<a name="instance"></a>

!!! variable "static PokemonFactory instance"

    @brief Constructs the singleton Pokémon factory.
           Initializes the internal storage for loaded Pokémon.
    @brief Retrieves the global instance of the Pokémon factory.
    
    :material-keyboard-return: **Return**
    :    Reference to the singleton PokemonFactory.
    

### m<a name="m"></a>

!!! variable "auto&amp; m"

    @brief Retrieves a loaded Pokémon by its name.
    
    :material-location-enter: `name`
    :    The name key used when loading from CSV.
    
    :material-keyboard-return: **Return**
    :    A copy of the corresponding Interactables::Pokemon.
    
    !!! note
     If the name is not found, prints an error and exits(1).
    

### output<a name="output"></a>

!!! variable "std::vector&lt;Interactables::Joueur&gt; output"

    @brief Reads all players from a CSV file and constructs Joueur instances.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing player data.
                    The file is expected to have a header line followed by lines of the form:
                    `name,pokemon1,pokemon2,...,pokemon6`.
    
    :material-keyboard-return: **Return**
    :    A std::vector of Interactables::Joueur objects populated from the CSV.
                Exits the program with code 1 if the file cannot be opened.
    

### output<a name="output"></a>

!!! variable "std::vector&lt;Interactables::LeaderDeGym&gt; output"

    @brief Reads all Gym Leaders from a CSV file and constructs LeaderDeGym instances.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing gym leader data.
                    The file is expected to have a header line followed by lines of the form:
                    `name,gymName,badge,pokemon1,...,pokemon6`.
    
    :material-keyboard-return: **Return**
    :    A std::vector of Interactables::LeaderDeGym objects populated from the CSV.
                Exits the program with code 1 if the file cannot be opened.
    

### output<a name="output"></a>

!!! variable "std::vector&lt;Interactables::MaitrePokemon&gt; output"

    @brief Reads all Master Trainers from a CSV file and constructs MaitrePokemon instances.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing master trainer data.
                    The file is expected to have a header line followed by lines of the form:
                    `name,pokemon1,pokemon2,...,pokemon6`.
    
    :material-keyboard-return: **Return**
    :    A std::vector of Interactables::MaitrePokemon objects populated from the CSV.
                Exits the program with code 1 if the file cannot be opened.
    

### output<a name="output"></a>

!!! variable "std::vector&lt;Interactables::Pokemon&gt; output"

    @brief Returns all Pokémon currently loaded in the factory.
    
    :material-keyboard-return: **Return**
    :    A std::vector containing copies of every loaded Pokémon.
    

## Function Details

### file<a name="file"></a>
!!! function "std::ifstream file(path)"

    @brief Loads Pokémon definitions from a CSV file into the factory.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing Pokémon data.
                    The first line is treated as a header and skipped.
                    Each subsequent line must have the form:
                    `name,type1,type2,hp,attack,attackDamage`.
    
    !!! note
     On I/O failure or malformed file, prints an error and exits(1).
    

