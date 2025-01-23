# Kalman-Filter-Project

*Overview*
This MATLAB script records audio for a specified duration, applies a Kalman filter for noise reduction, and visualizes the results in both the time and frequency domains. The filtered audio is saved as a file, and playback options are provided for both the original and processed audio signals.

*Features*
1.Audio Recording:
Records a mono audio signal with specified parameters (sampling frequency, bits per sample, and duration).
2.Kalman Filter Implementation:
Reduces noise in the recorded audio using a basic Kalman filter algorithm.
3.Visualization:
Plots the recorded and filtered audio in both the time and frequency domains for comparison.
4.Audio Playback:
Enables playback of both the original and Kalman-filtered audio signals.
5.Output:
Saves the Kalman-filtered audio as a .wav file for further use.

*Usage Instructions*
1.Set Recording Parameters:
Sampling frequency (fs): Default is 44,100 Hz (CD quality).
Bits per sample (bitsPerSample): Default is 16.
Number of channels (numChannels): Set to 1 (mono).
Recording duration (recordingDuration): Default is 15 seconds.
2.Run the Script:
Execute the script in MATLAB to start recording. A message prompts the user to begin speaking.
3.Noise Reduction:
The Kalman filter parameters (processNoise and measurementNoise) can be adjusted to fine-tune the noise reduction process.
4.View Results:
Time and frequency domain plots for both the original and filtered signals are displayed.
5.Save and Playback:
The filtered audio is saved as recorded_audio_noise_reduced.wav.
Both the original and filtered audio can be played back within MATLAB.

*Dependencies*
MATLAB with support for audiorecorder, audioplayer, and plotting functions.
FFT-related functions for frequency domain analysis.

*Key Sections of the Script*
1.Audio Recording:
Utilizes audiorecorder to capture audio and recordblocking for synchronous recording.
2.Kalman Filter:
A basic implementation to estimate and correct noisy signals based on recursive predictions and updates.
3.Plotting:
subplot is used to display side-by-side comparisons of audio signals in time and frequency domains.
4.Audio Output:
Saves the processed audio to a .wav file using audiowrite.

*Customization*
1.Adjust Kalman Filter Parameters:
processNoise and measurementNoise control the sensitivity of the noise reduction process.
2.Modify Recording Duration:
Change the recordingDuration variable to record for a longer or shorter time.
3.Save Outputs:
The file name of the saved audio can be customized in the audiowrite function.

*Example Plots*
1.Time Domain:
Comparison of the original and filtered audio waveforms.
2.Frequency Domain:
Visualization of the frequency spectrum before and after noise reduction.
3.Known Limitations:
The Kalman filter assumes a constant process and measurement noise, which may not perform well with varying noise types or levels.
The script does not handle stereo audio.

*Future Enhancements*
1.Add support for stereo audio recording and processing.
2.Implement an adaptive Kalman filter for better performance with varying noise.
3.Enhance visualization with interactive plots.
