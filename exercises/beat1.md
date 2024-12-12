---
title: Exploring Beat Frequency and more
layout: default
---

# Exercise 3: Exploring Beat Frequency
# Objective

The goal of this exercise is to explore the phenomenon of beat frequency
using stereo sounds in Praat. You will combine sine waves with slightly
different frequencies, observe the formation of beats, and investigate
how our auditory system perceives these beats differently based on how
the sound is created. **There is no submission required; focus on
experimenting and understanding.** You are expected to know the basic
concept of beat frequencies for your final exam.

# Understanding Beat Frequency

Beat frequencies occur when two sound waves with slightly different
frequencies interfere, creating a tone that fluctuates in volume between
loud and soft. This fluctuation is known as **beats**. The phenomenon
arises from the constructive and destructive interference between the
two waves.  
When two waves are expressed mathematically as:

*x*<sub>1</sub> = *A*cos (*ω*<sub>1</sub>*t*)  and  *x*<sub>2</sub> = *A*cos (*ω*<sub>2</sub>*t*),

their sum can be simplified using a trigonometric identity, leading to:

*x* = *x*<sub>1</sub> + *x*<sub>2</sub> = 2*A*cos (*ω*<sub>mod</sub>*t*)cos (*ω*<sub>avg</sub>*t*),

where:

-   $\omega\_\text{avg} = \frac{\omega_1 + \omega_2}{2}$: **average
    angular frequency**

-   $\omega\_\text{mod} = \frac{\omega_1 - \omega_2}{2}$: **modulation
    angular frequency**

For beat frequencies to occur, the two angular frequencies must be close
in value. Mathematically, this condition can be expressed as:
\|*ω*<sub>1</sub> − *ω*<sub>2</sub>\| ≪ *ω*<sub>1</sub> + *ω*<sub>2</sub>
This implies that the average angular frequency, *ω*<sub>avg</sub>, is
approximately equal to *ω*<sub>1</sub> or *ω*<sub>2</sub>, while the
modulation angular frequency, *ω*<sub>mod</sub>, is very small,
approaching zero. As a result, the cos (*ω*<sub>mod</sub>*t*) term
oscillates very slowly. Combined with the amplitude term 2*A*, the
product 2*A*cos (*ω*<sub>mod</sub>*t*) provides a slowly varying
amplitude for the cos (*ω*<sub>avg</sub>*t*) function.

The beat frequency is found to be twice the modulation frequency,
*f*<sub>mod</sub>, where
$f\_{\text{mod}} = \frac{\omega\_{\text{mod}}}{2\pi}$. Thus, we have:
*f*<sub>beat</sub> = 2 ⋅ *f*<sub>mod</sub> = *f*<sub>1</sub> − *f*<sub>2</sub>

This means the rate of amplitude modulation (i.e., the number of beats
per second) corresponds to the absolute frequency difference between the
two waves.

The formation of beats is illustrated in the figure below. The upper
graph shows the signal at frequency *f*<sub>1</sub>, the middle graph
shows the signal at frequency *f*<sub>2</sub>, and the bottom graph
represents the sum of the two signals, with *f*<sub>1</sub> and
*f*<sub>2</sub> very close to each other in value. The peaks and troughs
of the beats are separated by one beat period, as indicated in the
figure.

<figure id="fig:beat">
<p><img src="beat-phenomenon.png" alt="image" /> <span id="fig:beat"
data-label="fig:beat"></span></p>
</figure>

# Exercise Instructions

Follow the steps below to create and explore beat frequencies in Praat.

## Step 1: Create Stereo Sound with Identical Channels

1\. Open Praat and go to `New` → `Sound` →
`Create Sound from formula...`.

. Use the following parameters in the pop-up window:

-   **Name:** `stereoIdentical`

-   **Number of channels:** `Stereo`

-   **Start time (s):** `0`

-   **End time (s):** `2`

-   **Sampling frequency (Hz):** `44100`

-   **Formula:**
    `1/2 * sin(2*pi*200*x) + 1/2 * sin(2*pi*205*x)`

. Play the sound and examine the waveform. Since you just added two sine
waves with very close frequencies (200 Hz and 205 Hz), the resulting
sound has a beat frequency of 205 − 200 = 5 Hz. This beat frequency is
perceived as periodic variations in the intensity of the sound.
Additionally, observe that it produces a consistent beat pattern across
both channels because the sounds in both channels are identical.

## Step 2: Create a Stereo Sound with Different Frequencies in Each Channel

1\. Go to `New` → `Sound` → `Create Sound from formula...`.

. Use the following parameters in the pop-up window:

-   **Name:** `stereoDifferent`

-   **Number of channels:** `Stereo`

-   **Start time (s):** `0`

-   **End time (s):** `2`

-   **Sampling frequency (Hz):** `44100`

-   **Formula:**
    `if row = 1 then 1/2 * sin(2*pi*200*x) else 1/2 * sin(2*pi*205*x) endif`

The conditional expression in the formula directs channel 1 to have a
frequency of 200 Hz and channel 2 to have 205 Hz.

## Step 3: Listen with Headphones and Compare Perception

1\. Listen to the sound using stereo speakers. You should hear beats
caused by the interaction of the two frequencies.

. Use headphones and listen separately with the left ear and then with
the right ear. You will hear slightly different tones in each channel.

. Listen with both ears using headphones. You will perceive beats, which
are not in the audio signal but are constructed in your brain. In
contrast to the beats in the previous step, which were present in the
audio signals reaching your ears, these beats are created solely by your
brain.

. Experiment with other values to create beats with different
frequencies. For example, try to create beats with 1 Hz and 15 Hz, and
observe how the beat frequency changes as you adjust the difference
between the two frequencies.

# Conclusion

This exercise demonstrates the phenomenon of beat frequencies and how
they are perceived differently based on the listening context. When
listening with both ears, our brain integrates the two slightly
different frequencies to create a unified perception of beats. This
activity highlights how auditory perception involves both the physical
properties of sound waves and the processing capabilities of the brain.