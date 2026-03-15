**Smart Audio Quality Enhancement System for Podcast Production **

This MATLAB-based toolkit provides an automated, professional-grade audio processing pipeline for podcast creators. It applies advanced Digital Signal Processing (DSP) techniques to clean up raw audio, remove background noise, and apply equalization and compression—achieving studio-quality results without the need for expensive hardware.

As a bonus, this repository includes several interactive demonstrations of fundamental DSP concepts, making it a great resource for both audio engineers and signal processing students.

✨ Key Features
🎧 Audio Processing Pipeline
The core enhancement system pushes raw audio through a 6-step professional processing chain:

Spectrum Analysis: Utilizes Welch's method to estimate the Power Spectral Density (PSD) and characterize background noise.

High-Pass Filtering: Applies a Kaiser-windowed FIR filter to eliminate low-frequency room rumble and mic handling noise.

Noise Reduction: Implements spectral subtraction to intelligently reduce background hiss and static.

Professional EQ: Uses cascaded IIR biquad filters to apply a broadcast-standard equalization curve, enhancing vocal clarity.

Dynamic Range Compression: Smooths out volume inconsistencies, ensuring the speaker's voice remains present and level.

Final Limiting & Normalization: Applies soft limiting to prevent digital clipping and normalizes the final output to -1 dBFS.

📚 Educational DSP Demonstrations
Alongside the main pipeline, the script includes practical demonstrations of core DSP principles:

Linear vs. Circular Convolution: Analyzes the differences and error margins between standard convolution and DFT-based zero-padded circular convolution.

Windowing Techniques: Compares Rectangular, Hann, Hamming, Blackman, Kaiser, and Triangular windows for spectral analysis.

DTMF Generation: Synthesizes standard Dual-Tone Multi-Frequency (dial pad) signals.

Sample Rate Conversion: Demonstrates upsampling (interpolation) and downsampling (decimation) handling.

DFT/IDFT Properties: Verifies perfect reconstruction and demonstrates frequency-domain low-pass filtering.

🚀 Getting Started
Prerequisites
To run this project, you will need:

MATLAB (R2021a or newer recommended)

Signal Processing Toolbox (Required for functions like pwelch, spectrogram, fir1, and resample)

Audio Toolbox (Recommended for the real-time audio streaming demonstration)

Installation & Usage
Clone this repository to your local machine.

Open MATLAB and navigate to the project directory.

Add a raw audio file named raw_podcast_audio.wav to the same folder.

Note: If no file is found, the system will automatically generate a highly realistic synthetic audio file complete with speech harmonics, 60Hz electrical hum, background noise, and room rumble to process.

Run the main script from the MATLAB command window:

Matlab
podcast_enhancer
📊 Outputs and Analysis
When the script finishes running, it will generate the following assets in your directory:

Audio Files:

enhanced_podcast_audio.wav: Your final, studio-ready podcast track.

linear_convolution_demo.wav: Result of the convolution reverb demo.

dtmf_test_sequence.wav: The generated DTMF tone sequence.

interpolated_[Hz].wav & decimated_[Hz].wav: Sample rate conversion results.

Visual Analytics:
A comprehensive UI figure will open, displaying:

Time Domain Comparison (Original vs. Enhanced)

Frequency Domain Comparison via FFT

Power Spectral Density Analysis

A detailed Spectrogram of the enhanced audio

Dynamic Range comparison charts

Signal-to-Noise Ratio (SNR) improvements

🛠️ Configuration
You can easily tweak the pipeline for your specific microphone or voice type by modifying the setup_enhancement_parameters() function inside the script. Adjustable parameters include:

Noise reduction factor and spectral floor.

High-pass and low-pass filter cutoffs.

Specific EQ band frequencies and gains.

Compression ratio and threshold thresholds.
