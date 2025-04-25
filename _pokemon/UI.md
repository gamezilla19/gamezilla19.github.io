---
generator: doxide
---


# UI

**class UI**

@brief Controls global UI I/O actions.
(Will) Implement stuff like human-like typeing, boxed display...


## Functions

| Name | Description |
| ---- | ----------- |
| [boxed](#boxed) |  !!! note Expect 1len strings for {upper,lower}_{left,right} and {vertical,horisontal}_border  |

## Function Details

### boxed<a name="boxed"></a>
!!! function "static std::string boxed(const std::string&amp; text, const std::string&amp; align              = &quot;left&quot;, // &quot;left&quot;, &quot;center&quot;, &quot;right&quot; const std::string&amp; upper_left         = &quot;╭&quot;, const std::string&amp; upper_right        = &quot;╮&quot;, const std::string&amp; lower_left         = &quot;╰&quot;, const std::string&amp; lower_right        = &quot;╯&quot;, const std::string&amp; vertical_border    = &quot;│&quot;, const std::string&amp; horisontal_border  = &quot;─&quot; )"

    
    !!! note
     Expect 1len strings for {upper,lower}_{left,right} and {vertical,horisontal}_border
    

