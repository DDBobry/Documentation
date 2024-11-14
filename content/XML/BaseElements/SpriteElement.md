+++
title = '<Sprite>'
type = 'docs'
+++

In **ZTD**, **sprites** are used to define the visual appearance of entities such as buildings, enemies, and other game objects. The `<Sprite>` element in the XML configuration file is responsible for specifying the size, color, opacity, and texture of an entity's sprite.

---

## Components

{{% expand title="Width and Height" %}}

```xml
<Property name="Width" value="0.1" />
<Property name="Height" value="0.3" />
```

- **Width**: The width of the sprite in game units. This value defines how wide the sprite is when rendered. The value `0.1` would represent a small width, while larger numbers would make the sprite larger.
- **Height**: The height of the sprite in game units. This works similarly to `Width` and controls how tall the sprite is. A value of `0.3` would make it relatively taller than its width.


| Property       | Type              | Min Value | Max Value | Default Value |
|----------------|-------------------|-----------|-----------|---------------|
| **Width**      | Float (unsigned)  | 0.1         | 10         | -             |
| **Height**     | Float (unsigned)  | 0.1         | 10         | -             |

{{% /expand %}}

{{% expand title="Opacity" %}}

```xml
<Property name="Opacity" value="1" />
```

- **Opacity**: Defines how transparent or opaque the sprite appears. The value `1` means fully opaque (no transparency), while `0` would make the sprite completely transparent. Intermediate values, such as `0.5`, make the sprite semi-transparent. 

- **Default**: If the `Opacity` property is not defined, the default value is `1` (fully opaque). This means the sprite will be fully visible unless specified otherwise.

| Property       | Type              | Min Value | Max Value | Default Value |
|----------------|-------------------|-----------|-----------|---------------|
| **Opacity**    | Float     | 0         | 1         | 1             |

{{% /expand %}}

{{% expand title="Color" %}}

```xml
<Color hex="#00FF00" />
<Color r="0" g="255" b="0" />
```

- **Hexadecimal Color**: The `<Color>` element allows you to specify the sprite’s color in either hexadecimal format (`hex="#00FF00"`) or RGB format (`r="0" g="255" b="0"`). 
  - **Hex format** (`hex="#00FF00"`): The hex value `#00FF00` represents a bright green color, where `FF` indicates maximum intensity of green.
  - **RGB format** (`r="0" g="255" b="0"`): Alternatively, you can specify the color using the RGB model, where `r`, `g`, and `b` represent the red, green, and blue components, respectively. In this case, a `0` value for red and blue, and a `255` value for green, produces the same green color.

- **Default**: If no color is provided, the default color is **white** (`#FFFFFF`).

| Property       | Type              | Min Value | Max Value | Default Value |
|----------------|-------------------|-----------|-----------|---------------|
| **Color**      | Hex or RGB        | -         | -         | `#FFFFFF`     |

{{% /expand %}}

{{% expand title="Texture" %}}

```xml
<Texture file="__base__/assets/textures/zombie.png" />
```

- **Texture**: This optional element specifies an image file to be used as the texture for the sprite. The `file` attribute points to the image location, typically in the game's asset folder. For example, the texture file `__base__/assets/textures/zombie.png` could be the image of a zombie, which will be used to represent the enemy sprite. 
- **Optional**: If the `<Texture>` element is not provided, the sprite will be rendered using the above-defined `<Color>`.

| Property       | Type              | Min Value | Max Value | Default Value |
|----------------|-------------------|-----------|-----------|---------------|
| **Texture**    | String (filepath) | -         | -         | -             |

{{% /expand %}}

## Example

Here’s an example of how the sprite for a zombie might be configured in the game:

```xml
<Sprite>
    <Property name="Width" value="0.1" />
    <Property name="Height" value="0.3" />
    <Property name="Opacity" value="1" />
    
    <Color hex="#00FF00" />  <!-- Green color -->
    <Texture file="__base__/assets/textures/zombie.png" />
</Sprite>
```

- **Width** and **Height** are set to scale the zombie sprite's size.
- **Opacity** is set to `1` for full visibility (default value).
- **Color** is set to green (`#00FF00`).
- **Texture** points to an image of a zombie.
