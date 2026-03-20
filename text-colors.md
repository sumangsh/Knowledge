# 🎨 1️⃣ Standard ANSI Foreground Colors (30–37)

|Code|Color|
|------|------|
|30|Black|
|31|Red|
|32|Green|
|32|Yellow|
|34|Blue|
|35|Magenta|
|36|Cyan|
|37|White|

```
"`e[30mBlack`e[0m"
"`e[31mRed`e[0m"
"`e[32mGreen`e[0m"
"`e[33mYellow`e[0m"
"`e[34mBlue`e[0m"
"`e[35mMagenta`e[0m"
"`e[36mCyan`e[0m"
"`e[37mWhite`e[0m"
```


# 🌈 2️⃣ Bright Foreground Colors (90–97)

|Code|Color|
|------|------|
|90|Bright Black (Gray)|
|91|Bright Red|
|92|Bright Green|
|92|Bright Yellow|
|94|Bright Blue|
|95|Bright Magenta|
|96|Bright Cyan|
|97|Bright White|


```
"`e[90mBright Black (Gray)`e[0m"
"`e[91mBright Red`e[0m"
"`e[92mBright Green`e[0m"
"`e[93mBright Yellow`e[0m"
"`e[94mBright Blue`e[0m"
"`e[95mBright Magenta`e[0m"
"`e[96mBright Cyan`e[0m"
"`e[97mBright White`e[0m"
```

# 🎨 3️⃣ Background Colors (40–47)

|Code|Color|
|------|------|
|40|Black|
|41|Red|
|42|Green|
|42|Yellow|
|44|Blue|
|45|Magenta|
|46|Cyan|
|47|White|

```
"`e[41mRed Background`e[0m"
```

# 🌈 4️⃣ Bright Background Colors (100–107)

| Code | Bright Background |
| ---- | ----------------- |
| 100  | Bright Black      |
| 101  | Bright Red        |
| 102  | Bright Green      |
| 103  | Bright Yellow     |
| 104  | Bright Blue       |
| 105  | Bright Magenta    |
| 106  | Bright Cyan       |
| 107  | Bright White      |


# 🎯 5️⃣ 256-Color Mode (Extended)

__This is like choosing a color from a 256 predefined color palette__

__How it works__

- Colors are chosen from a fixed palette of 256 colors
- The terminal maps the index (0–255) to a predefined color
- You cannot customize the RGB values

__Format__

_Forground_

- 38 = set foreground color
- 5 = use indexed color mode
- <n> = number from 0–255

_Background_

- 48 = set background color
- 5 = use indexed color mode
- <n> = number from 0–255
  
```
"`e[38;5;196mThis is bright red (indexed)`e[0m"
"`e[48;5;196mThis is bright red (indexed)`e[0m"
```

```
# Ensure ANSI escape support
$esc = [char]27

Write-Host "ANSI 256 Color Table" -ForegroundColor Cyan
Write-Host ""

for ($i = 0; $i -lt 256; $i++) {

    # Print color block with index
    Write-Host -NoNewline "$esc[38;5;${i}m $("{0:D3}" -f $i) $esc[0m "

    # New line every 16 colors for clean grid
    if (($i + 1) % 16 -eq 0) {
        Write-Host ""
    }
}

Write-Host ""
Write-Host "`nDone." -ForegroundColor Green
```

# 🌈 6️⃣ True Color (24-bit RGB)

__Think of it like using a full RGB color picker instead of a limited palette__

__How it works__

- You specify the exact RGB value
- Supports 16,777,216 colors (256³)
- Much smoother gradients
- More modern terminals required


__Format__

_Forground_
- 38 = set foreground
- 2 = use 24-bit RGB mode
- R, G, B = values from 0–255

_Background_
- 48 = set foreground
- 2 = use 24-bit RGB mode
- R, G, B = values from 0–255

```
"`e[38;2;255;87;51mCustom orange color`e[0m"
"`e[48;2;255;87;51mCustom orange color`e[0m"
```

```
$esc = [char]27
$width = 80
$height = 24

for ($y = 0; $y -lt $height; $y++) {
    for ($x = 0; $x -lt $width; $x++) {

        $r = [int](255 * $x / $width)
        $g = [int](255 * $y / $height)
        $b = [int](255 * (1 - $x / $width))

        Write-Host -NoNewline "$esc[48;2;${r};${g};${b}m "
    }
    Write-Host "$esc[0m"
}

```
