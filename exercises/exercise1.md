# Creating Complex Sounds from Simple Sine Waves in Praat

### Experimental Phonetics (Autumn 2024)
**Instructor**: H. Rahmani

---

## Objective
In this exercise, you'll learn how to create a sound using sine waves. You'll begin by creating a single sine wave and gradually add more sine waves. As you add more, observe the changes in the sound and its shape. Eventually, you will notice that the sound you are creating resembles a new kind of wave, known as a **sawtooth wave**. Below are the visual representations of a sine wave and a sawtooth wave for comparison.

### Visualizing the Waves
Here’s an example of what sine and sawtooth waves look like:

![Sine Wave and Sawtooth Wave](example-image.png)

---

> **Warning**  
> Since you are about to create audio waves, you have to be careful with the sound levels. Keep your computer's volume at a reasonable level before playing any sounds to avoid damaging your hearing or hardware. Start with a low volume and adjust only after assessing the sound.

---

## Step 1: Creating a Simple Sine Wave

1. Open **Praat** and go to `New > Sound > Create Sound from formula...`.
2. In the dialog box, use the following parameters:
   - **Name**: Enter a name for your sound (e.g., `sineWave`).
   - **Start time (s)**: Set it to `0`.
   - **End time (s)**: Set it to `1` (for a 1-second sound).
   - **Sampling frequency (Hz)**: Set it to `44100 Hz`.
   - **Formula**: Enter the formula to create a basic sine wave:
     ```mathematica
     0.5 * sin(2 * pi * 440 * x)
     ```
3. This creates a sine wave with a frequency of 440 Hz (a standard A note). The factor `0.5` ensures the amplitude of the resulting sound stays within the acceptable range in Praat.
4. Click `OK` and then play the sound to hear the pure sine wave.

---

## Step 2: Adding a Second Sine Wave (First Harmonic)

1. Next, we’ll add another sine wave that has a higher frequency, known as a harmonic.
2. Go back to `New > Sound > Create Sound from formula...`.
3. In the dialog box, use the following formula to add the first harmonic:
   ```mathematica
   0.5 * (sin(2 * pi * 440 * x) + (1/2) * sin(2 * pi * 880 * x))

