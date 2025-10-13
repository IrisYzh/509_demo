# Music Composer Solution
This project explores how to design a **music composer** in **Python**  that can automatically creates short melodies using algorithmic logic.

## Input
#### This program is designed to combine user input with automatic generation to create a personalized melody. 

1. When the program starts, it first asks the user to enter their birthday.

2. The program then processes the birthday data to generate internal parameters for music composition, such as:
- **Key/scale:** derived from the month or day (e.g., May → G major).
- **Tempo (BPM):** calculated from the sum or pattern of the digits in the birthday.
- **Length of the melody:** determined by the year of birth.
- **Starting note or mood:** could vary depending on whether the birthday falls in a certain season or range.

> _In this way, each user’s birthday leads to a unique set of musical properties, while the rest of the process is handled automatically by the composer logic._

## Output
#### After processing the user’s birthday, the program automatically generates a melody based on the computed musical parameters.

The output could be a piece of music sheet like this example:

![HBD](https://www.davidsides.com/cdn/shop/files/43.HappyBirthdayToYou.png?v=1704762933)

> _The final result is a unique melody that reflects the user’s birthday, blending personal data with algorithmic creativity._

## Representation
#### The program represents musical notes using a structured data format that captures both pitch and duration.

- Pitch representation:  
  - Each note is represented by its note name and octave, such as C4, E4, or A5.
  - These notes belong to a scale (e.g., C major, G major) determined by the user’s birthday data.
  - For example, the month might decide the scale (e.g., “May” → G major), and the day might influence the starting pitch.

- Duration representation:  
Time is captured using numerical values that represent beats:  
  - Quarter note → 0.5
  - Half note → 1.0
  - Whole note → 2.0

## Logic
#### The logic combines birthday-based rules with random generation to create a melody that is both structured and unique.

There are 3 rules helping the program decide what note comes next:

**1. Birthday-based rules:**
- The month defines the musical key.
- The day may affect the range or starting pitch.  
- The year digits might determine rhythmic diversity or tempo category.

**2. Melodic patterning:**
- Favor stepwise motion for smoother flow.
- Occasionally add a skip or repetition for variation.

**3. Controlled randomness:**
- Randomness is used within defined constraints to avoid monotony while ensuring predictability.

> _The program stops generating once the total note count or total duration (in beats) reaches a target. This ensures the resulting sheet has a consistent length, similar to a short musical phrase._

## Extensions
#### As the goal is to create printable sheet music, extending the project toward more structured or expressive scores faces several challenges:

- **Musical form and repetition:**  
Simple random or rule-based note generation works for short melodies, but longer compositions need recognizable patterns — verses, motifs, and repetition.

- **Rhythmic balance:**  
Ensuring each measure has a consistent beat sum requires additional logic for time signature management.