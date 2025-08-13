# Kyaa UI Library

**Version:** 1.1 BETA-A4J1-0J6E

Kyaa UI Library is a lightweight and flexible Roblox UI library that lets you quickly create windows, tabs, buttons, toggles, sliders, dropdowns, and notifications. It's designed to work well on both desktop and mobile screens.

## Notes

- `useScroll = true` is recommended for mobile devices; `false` is better for desktop.
- Notifications, labels, errors, buttons, toggles, textboxes, sliders, and section (BETA) are fully supported.
- TextBox `deleteOnFocus = true` clears placeholder when focused.

## Changelog

**1.1 BETA-A4J1-0J6E**

not this time.

## Loading the Library

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/kyaarb/UiLib/main/KyaaUiLib.lua"))()
```

## Creating a UI Window

```lua
local ui = Library:CreateWindow(
    "My Window",    -- Window title
    true,           -- useScroll: true for mobile, false for auto-height (desktop)
    true            -- Use Loading animation (wait for 1.2 Update to work)
)
```

## Notifications

```lua
ui:Notify(
    "Success",                           -- Title
    "Data Saved",                         -- Subtitle
    "Your progress has been saved successfully.",  -- Main content
    5                                     -- Duration (seconds)
)
```

## Labels and Error Messages

```lua
ui:Label("This is a simple label.\nKyaa Ui Library")
ui:Error("Failed to load data!")
```

## Tabs

```lua
ui:Tab("====Main Menu====")
```

## Dropdowns

```lua
ui:Dropdown(
    "Number",
    {"One", "Two", "Three","Four","Five","Six","Seven"},
    0,
    function(selectedItem)
        print("Selected: " .. selectedItem)
    end,
    false
)
```

## Buttons

```lua
ui:Button("Click Me", function()
    print("Button was clicked!")
end)
```

## Toggles

```lua
ui:Toggle(
    "Enable Music",
    true,
    function(state)
        if state then
            print("Music enabled")
        else
            print("Music disabled")
        end
    end
)
```

## Text Boxes

```lua
ui:CreateTextBox(
    "Username",
    "Enter your username...",
    function(text)
        print("User typed: " .. text)
    end,
    true
)
```

## Sliders

```lua
ui:Slider(
    "Volume",
    0,
    100,
    50,
    function(value)
        print("Volume is now: " .. value)
    end
)
```
## Sections

Still in development!

## Example Script

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/kyaarb/UiLib/main/KyaaUiLib.lua"))()

local ui = Library:CreateWindow(
    "My Window",    -- Window title
    true,           -- useScroll: true for mobile, false for auto-height (desktop)
    true            -- Use Loading animation (wait for 1.2 Update to work)
)

ui:Label("This is a simple label.\nKyaa Ui Library")

ui:Error("Failed to load data!")

ui:Tab("Main Menu")

ui:Dropdown(
    "Number",
    {"One", "Two", "Three","Four","Five","Six","Seven"},
    0,
    function(selectedItem)
        print("Selected: " .. selectedItem)
    end,
    false
)

ui:Button("Click Me", function()
    print("Button was clicked!")
    ui:Notify(
        "Success",                           -- Title
        "Callback",                         -- Subtitle
        "Button was clicked!.",  -- Main content
    5                                     -- Duration (seconds)
)
end)

ui:Toggle(
    "Enable Music",
    true,
    function(state)
        if state then
            print("Music enabled")
        else
            print("Music disabled")
        end
    end
)

ui:CreateTextBox(
    "Username",
    "Enter your username...",
    function(text)
        print("User typed: " .. text)
    end,
    true
)

ui:Slider(
    "Volume",
    0,
    100,
    50,
    function(value)
        print("Volume is now: " .. value)
    end
)
```

## 1.2 Leak

Fixing Bugs
end.. lol

# Issues and Support

If you encounter any issues while using this, please report them on our Discord server: [discord.gg/kymU65UvNb](https://discord.gg/kymU65UvNb)
