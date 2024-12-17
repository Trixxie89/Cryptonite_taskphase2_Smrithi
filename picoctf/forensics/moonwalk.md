# M00NWALK
picoCTF{beep_boop_im_in_space}
## step 1
The hint suggests that this is related to how images from the moon landing were transmitted back to earth. Some research leads to SSTV. Note: Originally I solved this challenge using this program for Windows but since then I found an easier way that works within Kali Linux (see next step).
Install qsstv with apt-get install qsstRun pactl load-module module-null-sink sink_name=virtual-cable
Run pavucontrol. A GUI will pop-up, go to the "Output Devices" tab to verify that you have the "Null Output" device.Run qsstv. The program GUI will pop-up, go to Options to Configuration" -tp"Sound" and select the PulseAudio Audio Interface Back in the pavucontrol GUI, select the "Recording" tab and specify that QSSTV should capture audio from the Null Output.The hint asked "What is the CMU mascot?" - the answer is "Scotty the Scottie Dog". This hinted that we should select "Scottie 1" as QSSTV's "Mode". Select "Auto Slant" as well.Run paplay -d virtual-cable message.wav to create the image: 
this task was difficult for me..and even after getting flag..it was hard for me to understand what was happening
## whati learnt
This challenge was about decoding an image hidden in an audio file using SSTV (Slow Scan Television), a method used to transmit images over audio signals, famously during the moon landing. The audio file (message.wav) contained SSTV-encoded data, and tools like QSSTV and PulseAudio were used to decode it. First, a virtual audio cable was created with pactl load-module to route the audio output to QSSTV. Using pavucontrol, the audio routing was configured to send the playback to the virtual sink, allowing QSSTV to capture and decode the audio. The challenge hinted at using "Scottie 1" mode in QSSTV, which matches a specific SSTV encoding format, and playing the audio with paplay enabled the decoding process. QSSTV then processed the SSTV signal and revealed the hidden image. This challenge demonstrated how audio can carry visual data, requiring both knowledge of SSTV formats and virtual audio routing. It also reinforced concepts of digital signal processing and real-world data transmission techniques. While initially complex, it showed how modern tools can replicate techniques used in historic space missions. This was a great way to learn audio-to-image decoding and explore SSTV technology!
## other methods
nonw
## refernces
https://picoctf2019.haydenhousen.com/forensics/m00nwalk






