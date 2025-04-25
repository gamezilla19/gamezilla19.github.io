---
generator: doxide
---


# EntrainersFactory

**class EntrainersFactory**

@brief Factory class for loading different types of trainers from CSV files.


## Functions

| Name | Description |
| ---- | ----------- |
| [getJoueursFromCSV](#getJoueursFromCSV) | @brief Loads player (Joueur) data from a CSV file. |
| [getLeadersFromCSV](#getLeadersFromCSV) | @brief Loads gym leader (LeaderDeGym) data from a CSV file. |
| [getMaitresFromCSV](#getMaitresFromCSV) | @brief Loads master trainer (MaitrePokemon) data from a CSV file. |

## Function Details

### getJoueursFromCSV<a name="getJoueursFromCSV"></a>
!!! function "static std::vector&lt;Interactables::Joueur&gt; getJoueursFromCSV(const std::string&amp; path)"

    @brief Loads player (Joueur) data from a CSV file.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing player data.
                    The first line is treated as a header and skipped.
                    Each subsequent line must have the form:
                    `name,pokemon1,...,pokemon6`.
    
    :material-keyboard-return: **Return**
    :    A vector of Interactables::Joueur instances constructed from the file.
    @throws std::exit(1) if the file cannot be opened.
    

### getLeadersFromCSV<a name="getLeadersFromCSV"></a>
!!! function "static std::vector&lt;Interactables::LeaderDeGym&gt; getLeadersFromCSV(const std::string&amp; path)"

    @brief Loads gym leader (LeaderDeGym) data from a CSV file.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing gym leader data.
                    The first line is treated as a header and skipped.
                    Each subsequent line must have the form:
                    `name,gymName,badge,pokemon1,...,pokemon6`.
    
    :material-keyboard-return: **Return**
    :    A vector of Interactables::LeaderDeGym instances constructed from the file.
    @throws std::exit(1) if the file cannot be opened.
    

### getMaitresFromCSV<a name="getMaitresFromCSV"></a>
!!! function "static std::vector&lt;Interactables::MaitrePokemon&gt; getMaitresFromCSV(const std::string&amp; path)"

    @brief Loads master trainer (MaitrePokemon) data from a CSV file.
    
    :material-location-enter: `path`
    :    Filesystem path to the CSV file containing master trainer data.
                    The first line is treated as a header and skipped.
                    Each subsequent line must have the form:
                    `name,pokemon1,...,pokemon6`.
    
    :material-keyboard-return: **Return**
    :    A vector of Interactables::MaitrePokemon instances constructed from the file.
    @throws std::exit(1) if the file cannot be opened.
    

