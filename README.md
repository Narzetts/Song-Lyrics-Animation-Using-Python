Here's the README in English:

---

# Lyrics Typing Effect

## Description
This Python script displays song lyrics with a typing effect, where each letter appears one by one on the screen, followed by a specified delay before the next line is displayed.

## Features
- Displays each letter of the lyrics sequentially with a typing effect.
- Provides delays between each letter and each line of lyrics.
- Allows customization of the delay between letters and lines.

## Usage

1. **Import Module**
   This script uses the `time` module to manage delays.

   ```python
   import time
   ```

2. **Define Lyrics and Delays**
   Define a list of lyrics and the delay time for each line, as well as the delay between letters.

   ```python
   lyrics = [
       "I have faith in what i see",
       "Now I know i have met an angel",
       "in person",
       "And she looks perfect",
       "I don't deserve this",
       "You look perfect tonight"
   ]

   delays = [0.5, 2, 1, 1, 2, 2]  # Delay before the next line starts
   char_delay = 0.1  # Delay in seconds between each letter
   ```

3. **Define the Display Function**
   Define the `display_lyrics_with_typing_effect` function that will display the lyrics with the typing effect according to the specified timings.

   ```python
   def display_lyrics_with_typing_effect(lyrics, delays, char_delay):
       for i, line in enumerate(lyrics):
           for char in line:
               print(char, end='', flush=True)  # Display each letter without moving to a new line
               time.sleep(char_delay)  # Delay per letter
           print()  # Move to the next line after the whole sentence is displayed
           time.sleep(delays[i])  # Wait before proceeding to the next line
   ```

4. **Call the Function**
   Call the `display_lyrics_with_typing_effect` function with the predefined arguments.

   ```python
   display_lyrics_with_typing_effect(lyrics, delays, char_delay)
   ```

## Customization
- **Letter delay**: Adjust the `char_delay` value to speed up or slow down the typing effect.
- **Line delay**: Modify the `delays` list to change the waiting time between each line of lyrics.

## Example Output
```
I have faith in what i see
<waits...>
Now I know i have met an angel
<waits...>
...
```

