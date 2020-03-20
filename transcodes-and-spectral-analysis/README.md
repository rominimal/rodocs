---
description: Article is taken from Redacted Wiki
---

# Transcodes & Spectral Analysis

Note: For the purpose of this article, lossy master \(LM\) refers to both lossy web and lossy master.

This article attempts to better one's ability at recognizing lossy masters / transcodes. While it contains a lot of information, the ability to quickly distinguish lossy master from legitimate FLAC will only come from experience. This article will not transform a novice into an expert. Ask for help at [The "Is this a transcode?" thread](https://redacted.ch/forums.php?action=viewthread&threadid=2772) if you are confused or have doubts about a file's status as lossy or lossless.

Some tools exist to automatically determine whether or not something is legitimate lossless. Two such tools are Audio Identifier and auCDtect. They are useless. Discard all of them. Do not speak of them. Most importantly, **do not trust them.** They are not reliable indicators of quality and are wrong extremely often.

### Transcodes

When we obtain FLAC files, we expect them to not have any degradation in quality, to be "lossless" files. Unfortunately, FLAC files will sometimes contain lossy elements alongside lossless sections, or, even worse, be a bad transcode, meaning a lossy file transcoded to another format.

When a lossy file is converted to a lossless file, the data lost in the initial lossy compression process remains lost, and the lossless file is of the same fidelity as the lossy source file, but larger. This undermines the entire point of lossless audio. When a lossy file is transcoded into another lossy file, the lossy compression algorithms are run on the file again, resulting in more degradation than would occur if the algorithm were run on a lossless file. For that reason, one should never transcode lossy files.

The best way to identify transcodes is via spectral analysis, which is the examination of spectrograms, or spectrals, generated from the audio file. This page will introduce the process of identifying transcodes, alongside examples illustrating what one may see. Most of the example spectrals are generated with SoX.

### Lossy Masters

A lossy master is not an officially documented term, but rather a casual way of saying that the spectrogram view of lossless file, i.e., of the losslessly ripped flac track, does not live up to its expectations.

At worst, a lossy master is an officially released bad transcode by an artist, label, or distributor. At best, it is a lossless release with a non-negligible presence of lossy samples / lossy artifacts. The "lossiness" of a track can lie on a spectrum, but most of the time one will be able to determine whether or not a track is proper lossless, lossless with lossy samples, or a lossy master.

Proper lossless and lossless with lossy samples can be uploaded without a lossy master approval request. Lossy masters should always be reported for lossy master approval, and perhaps, depending on the quality, not be uploaded. Redacted has set a moderation precedent where files of poor quality, when sourced from an official distributor, can receive on-site approval. However, this does not mean that one should take advantage of this; albums transcoded from low-bitrate MP3s do not meet the quality standards embodied by Redacted, and the uploader should decide whether or not the files are worth uploading given their lossy nature.

Lossy masters can range from some artifacts in a FLAC file to a full-blown transcode. Some are, for the most part, lossless, while others are purely bad transcodes. When there is only very slight artifacting in the file \(e.g. several blocks here and there\) and the audio data is clearly lossless and extends for the full spectrum, without any other visible signs of degradation, it falls closer to the classification of "lossy samples." Generally, if one notices degradation from an unzoomed view, it is a lossy master. However, an unzoomed lossy master will not always have noticeable degradation. Tracks with many artifacts masked by noise should be reported for lossy master approval.

The lossy master flag serves two primary purposes. It protects a legitimately sourced upload from being reported as a bad transcode and deleted by a moderator and informs potential downloaders that the file is not completely lossless despite being in a lossless format. However, this flag is not necessary for files classified as "lossy samples". Since they are overwhelmingly lossless and clearly not transcodes, they do not require the protection offered by the flag. Instead of reporting those for lossy master approval, one can include information about the presence of lossy samples and spectrals in the torrent description.

Note: If the only lossy mastered tracks in a release are short intro/interlude/outro tracks, it does not fall under a lossy master or transcode.

### Lossless Files

Lossless files, to put it simply, contain all the audio data of the release. They lack the artifacts that lossy encoders create and, in many cases, have audio data that extends for the most to all of the frequency range. There are no rough, blocky cutoffs; if there is a cutoff, it is clean and sometimes more of a rolling off of audio data than a sharp cutoff.

Despite representing all the available audio data, lossless files can still have cutoffs. Luckily, mastering decisions to cut off the audio at certain frequencies do not create lossy artifacts, so even if the "loud" part of the spectral \(red/orange/pink colors in SoX\) ends early and segues into the "quiet" part of the spectral \(purple/blue in SoX\) before cutoff points below 21 kHz, it does not necessarily mean the file is a transcode. Due to cutoffs being applied by both mastering engineers and lossy encoders, the attributes of the cutoff are more telling than its location. When those lower frequency fade-outs are smooth, and blue/purple audio data can still be spotted above it without any lossy artifacting, you can safely assume a lossy encoder has not been run over the file.

However, you will sometimes see a few lossy artifacts inside a file that is mostly lossless. Some examples are included below. When we refer to "lossy samples," we refer to this. The file is overwhelmingly lossless, and the authenticity of the file cannot be doubted, but a few artifacts are present. Usually, this will be a few block artifacts coincide with a lot of lossless data. There are no artifacts that affect the entire track; only a section or certain sample.

#### **21.5 kHz cutoff \(Lossless\)**

![](../.gitbook/assets/image%20%2855%29.png)

![](../.gitbook/assets/image%20%2821%29.png)

#### **Early fade out &lt;19 kHz \(Lossless\)**

![](../.gitbook/assets/image%20%282%29.png)

![](../.gitbook/assets/image%20%2851%29.png)

#### **Lossless with noise shaping \(Lossless\)**

![](../.gitbook/assets/image%20%2824%29.png)

![](../.gitbook/assets/image%20%2879%29.png)

#### **Lossy samples, block artifacts & slight shelf \(Lossy samples\)**

![](../.gitbook/assets/image%20%2863%29.png)

![](../.gitbook/assets/image%20%2869%29.png)

#### **Data + Noise \(Lossless\)**

![](../.gitbook/assets/image%20%2849%29.png)

![](../.gitbook/assets/image%20%2888%29.png)

### Lossy Files

Lossy files are used to lower file sizes at the cost of bits. With the assistance of magic complicated algorithms, they can greatly reduce the size of an audio file while keeping it transparent. A transparent encode means that a human listener cannot tell the difference between the lossy file and its lossless source. Transcodes from lossless to lossy are **good.** Transcodes from lossy are **bad.** Some of these algorithms leave visible traces in a spectral, which we can use to determine some information about a track.

By definition, a lossy file cannot be reconstructed into its lossless source. Bits necessary for doing so have been removed from the file, and other bits manipulated to create a sound that sounds equivalent to the original, at least to humans. Out of all the mainstream encoders used by consumers of music, Redacted allows MP3 and AAC \(trumpable by MP3\).

### Lossy Identifiers & Artifacts

There are several important signs and patterns to look for when examining a spectral for lossiness. They are covered in this section.

### **Noise**

Noise is not a lossy artifact but is an important concept that should be covered early on.

Noise is random audio data that doesn't fit any pattern or resemble any meaningful audio data. It is sometimes present across an audio file. Noise is sometimes applied alongside dithering; a file can be a bad transcode yet have random noise in high frequencies. Noise patterns frequently added alongside dithering can be found in a later section.

Audio data in high frequencies is a good sign for a music file--lossy encoders, in order to preserve bits, do not have much use for audio data above 20kHz, the limit to human hearing. They employ various techniques to remove data in upper frequencies while maintaining transparency. Although it is a good sign, audio data in higher frequencies are not a guarantee that a file is lossless. Some encoders do not apply a lowpass filter \(AAC, LAME V0\) and others allow for that filter to be modified or removed entirely \(LAME\).

Do not confuse legitimate data with noise and vice versa. Examples of noise patterns can be found below.

### **Lowpass Filter / Cutoffs**

A lowpass filter \(LPF\), also known as a cutoff, is a sudden loss of audio above a certain frequency. Typically, only audio information that above a cutoff would be quiet noise and/or clipping bursts \(covered in a later section\). Cutoffs come from various sources, the most well-known one being lossy encoders. The MP3 encoder is known to create strong cutoffs at frequencies ranging from 16kHz to 20.5kHz. However, mastering engineers can also create a cutoff during the mastering process. Many people associate a 21kHz cutoff with lossless audio, but that is a dangerous assumption to make. The MP3 encoder can be told to cut off at a frequency higher than 21kHz, and a mastering engineer can make the decision to cut off at a frequency lower than 21kHz. What matters more than the location and presence of the cutoff are the shape and data surrounding the cutoff.

Generally, if a cutoff is very sharp and/or has lossy artifacts, the file can safely be presumed to be a lossy master or transcode. Cutoffs made by lossy encoders generally contain blocks and have, depending on the encoder, little to no noise above them. A more gradual fading out of energy in the higher frequencies without any lossy artifacts were most likely a decision made by the mastering engineer and can be assumed safe. There are also sharp cutoffs made by mastering engineers at many different frequencies. Unless the cutoff is at an unnecessarily low frequency or artifacts are present, they are not a definitive tell for a lossy master or transcode.

A track can have multiple cutoffs at different timestamps. It does not need to have a uniform cutoff across the entire track.

There may be random noise above a cutoff. It is neither a good or bad sign. A lack of any noise above a cutoff alongside other artifacts is reminiscent of a bad transcode though since a lossy encoder applied directly to a FLAC has no need for that noise.

See [this](https://wiki.hydrogenaud.io/index.php?title=High-frequency_content_in_MP3s) for an explanation of why most lossy encoders have a lowpass filter.

#### **12 kHz cutoff \(LM\)**

![](../.gitbook/assets/image%20%285%29.png)

![](../.gitbook/assets/image%20%2823%29.png)

#### **20 kHz cutoff \(MP3 320\)**

![](../.gitbook/assets/image%20%2813%29.png)

![](../.gitbook/assets/image%20%2883%29.png)

#### **21 kHz cutoff \(Lossless\)**

![](../.gitbook/assets/image%20%2874%29.png)

![](../.gitbook/assets/image%20%2833%29.png)

#### **Low cutoff with small blocks \(LM\)**  

![](../.gitbook/assets/image%20%2886%29.png)

![](../.gitbook/assets/image%20%2861%29.png)

**Shelves**

A shelf is similar to a cutoff in that it's at a specific frequency and horizontally visible across \(a portion of\) the spectral, but they have significant differences. Many conflate cutoffs and shelves, but each has their own attributes and resulting conclusions.

When audio data is significantly decreased above a certain frequency, but not cut off, it is called a shelf. Strong shelves do not typically occur in lossless files, but shelves are an important way of conserving bits in the lossy compression process. MP3, for example, has historically applied a shelf at 16kHz for all bitrates, reducing the amount audio information present in the upper frequencies until the cutoff is reached. Lossless files can have a reduction in audio data above a certain frequency, but it's extremely unlikely for it to be a visibly horizontal "line" across the file.

A shelf will be uncommon to see in a legitimately lossless file but is often present in lossy to lossless transcodes.

![](../.gitbook/assets/image%20%2830%29.png)

#### **Shelf at 16kHz \(MP3 320\)**

![](../.gitbook/assets/image%20%2843%29.png)

![](../.gitbook/assets/image%20%2819%29.png)

### **Blocks**

Blocks are the most telltale sign of a lossy master or transcode. They are small rectangular "blobs" present in the spectral, typically around the cusp of the cutoff or other areas at the fringe of audio data, and sometimes clustered with other blocks. They are very small, but the rectangular shape or clustering should be clearly visible. They will sometimes be obscured by other audio data nearby, but can still poke out. They can be present at many different volumes--sometimes they are very loud \(red/orange/pink in SoX\), other times they can be quiet \(purple/blue in SoX\). Regardless of volume, blocks are blocks.

Lossy encoders create blocks in the process of saving bits. It is purely a lossy compression technique, meaning their presence indicates that a lossy process was run on a sample or the file. However, not all lossy encoders create blocks at every bitrate, so a track can be transcoded without a single block.

#### **Looks lossless.. but isn't \(LM\)**

![](../.gitbook/assets/image%20%2877%29.png)

![](../.gitbook/assets/image%20%2862%29.png)

#### **Blocks above a low shelf \(LM\)**

![](../.gitbook/assets/image%20%2881%29.png)

![](../.gitbook/assets/image%20%2882%29.png)

#### **Blocks in a low cutoff \(LM\)**

![](../.gitbook/assets/image%20%2854%29.png)

![](../.gitbook/assets/image%20%2811%29.png)

#### **Transcode with noise \(LM\)**

![](../.gitbook/assets/image%20%2875%29.png)

![](../.gitbook/assets/image%20%2844%29.png)

#### **Very condensed blocking of noise \(MP3 320\)**

![](../.gitbook/assets/image%20%2872%29.png)

![](../.gitbook/assets/image%20%281%29.png)

#### **A few blocks inside a lossless track \(Lossy samples\)**

![](../.gitbook/assets/image%20%2876%29.png)

![](../.gitbook/assets/image%20%2865%29.png)

#### **Cutoff and blocks \(LM\)**

![](../.gitbook/assets/image%20%2827%29.png)

![](../.gitbook/assets/image%20%2847%29.png)

### **Tying The Signs Together**

Lossy encoders employ a myriad of techniques to reduce the file size while maintaining transparency. Spectrals are an imperfect art; we inspect the files for the visual cues that match the techniques of lossy encoders. Because lossy encoders frequently create shelves, cutoffs, and blocks, as well as remove unnecessary noise, we take those signs to mean that a file is lossy. When there are very obvious occurrences of those signs, it's easy to determine that something is lossy. When files begin to have some of these signs but not all, or have a pattern that may be one of these signs or not, it gets difficult.

In some cases, a definitive answer based on the spectral alone is not possible. When the spectral leaves doubts, the source of the file, the genres and styles, and the media it came from all can contribute to determining whether something is lossy or not. Information about a file can tip the scales from not very suspicious to very suspicious. Some AAC encoders, for example, can trim a file down to 320kbps but keep a spectral nearly identical to the FLAC \(note that this is not usually the case\). Unfortunately, sometimes there's no noticing that difference with mere spectral analysis, so having good and reliable sources for uploads is very important.

With experience comes a better ability to distinguish lossy from lossless. However, even some of the most experienced people at spectral analysis can be uncertain. If you are cannot come to a definitive conclusion, ask for help at [The "Is this a transcode?" thread](https://redacted.ch/forums.php?action=viewthread&threadid=2772).

For example, try to tell which one is 320 AAC \(libavcodec\) and which is FLAC.

#### **Full spectrals**

![](../.gitbook/assets/image%20%2818%29.png)

![](../.gitbook/assets/image%20%288%29.png)

#### **Zoomed spectrals**

![](../.gitbook/assets/image%20%2825%29.png)

![](../.gitbook/assets/image%20%2834%29.png)

#### **Answer**

The first spectral in each is lossless.  
****The second is AAC.

### Oddities

Alongside the main lossy artifacts that one may see, there are also other artifacts and patterns that arise in audio files. These are not indicative of a lossy file, although many display confusion over them and take them to be an indicator of a transcode.

#### **Clipping Bursts**

Clipping occurs when the volume of the track reaches the maximum level possible and creates an artifact in the spectral, which looks like a burst of loud audio extending vertically, usually going out of the frequency range. These are frequently found in music mastered loudly and are not lossy. They are, however, a good inspection point to see if a lossy encoder has touched the file.

#### **Clipping bursts \(LM\)**

![](../.gitbook/assets/image%20%2870%29.png)

![](../.gitbook/assets/image%20%2829%29.png)

#### **Heavily degraded lossy clipping \(LM\)**

![](../.gitbook/assets/image%20%2812%29.png)

![](../.gitbook/assets/image%20%283%29.png)

#### **Weird Harmonics**

Occasionally the harmonics of a file will display weirdly in a spectral. Although strange, these are not the byproduct of a lossy encoder.

#### **A loud zigzag \(Lossless\)**

![](../.gitbook/assets/image%20%2835%29.png)

![](../.gitbook/assets/image%20%2842%29.png)

#### **A quiet zigzag \(Lossless\)**

![](../.gitbook/assets/image%20%2867%29.png)

![](../.gitbook/assets/image%20%2860%29.png)

#### **Horizontal lines and bursts**

![](../.gitbook/assets/image%20%2840%29.png)

![](../.gitbook/assets/image%20%2859%29.png)

**CRT Monitors**

These are the cause of horizontal lines across a spectral, as they are sometimes present in a recording. They are not a lossy artifact.

#### **Examples**

![](../.gitbook/assets/image%20%2828%29.png)

![](../.gitbook/assets/image%20%2848%29.png)

#### **Quiet Tracks**

Some genres, such as Classical and Jazz, often have very quiet recordings. When examining the spectrals for quiet albums, most of the data will be blue and it can be very hard to spot data in the double-digit frequency ranges. That does not mean that a file is lossy--the unassuming nature of spectrals of quiet tracks does not equate to a degradation in quality.

![](../.gitbook/assets/image%20%2841%29.png)

#### **Noise Patterns**

As briefly mentioned in the noise section above, random noise can be present in the spectrals. There are several frequently-occurring noise patterns, each with their own distinct characteristics and causes for being present.

One should be wary around noise--since it can come from MQA, extra care should be given to ensure that the file is legitimate \(i.e. the noise is not because of it being or sourced from a MQA file\). [The "Is this a transcode?" thread](https://redacted.ch/forums.php?action=viewthread&threadid=2772) is available for the uncertain.

#### **Dither**

When FLACs of a higher bit depth are dithered to a lower bit depth, a noise shaping filter is sometimes applied. These create a haze of noise in a spectral. Example spectrals can be found at [http://sox.sourceforge.net/SoX/NoiseShaping](http://sox.sourceforge.net/SoX/NoiseShaping). The distinguishing characteristic of most noise added via this process is the volume level and the gradual rolling off of the noise.

This noise is not an indication of anything wrong with the audio file, but it can mask a lossy master. The presence of a noise-shaping caused haze in the upper ranges or a consistent noise does not mean that a release is lossless. A bad transcode or lossy master dithered from 24-bit to 16-bit with added noise can be confusing to spot; do not let the dither noise cause confusion.

#### **MQA**

These can look very similar to the noise made in the dithering process. However, the noise of MQA files has distinct visual clues which differentiate it from dither-caused noise. For example, MQA noise will typically shelve at around 19 kHz and 15 kHz, in a horizontally visible way. Although loud tracks will make it difficult to look for a shelf in MQA noise, the lead-outs are sometimes quiet enough to inspect for the shelves. The MQAid script can identify MQA files with certainty; however, it fails on downconverted, downsampled, and/or transcoded MQA files. In those cases, one should inspect the spectrals.

![](../.gitbook/assets/image%20%2817%29.png)

See [User Guide to Identifying MQA-encoded files](https://redacted.ch/wiki.php?action=article&id=365) for information about what the spectrals look like.

### Lossy to Lossy Transcodes

Lossy to lossy transcodes are either very easy or very difficult to spot. There are two primary ways in which a lossy to lossy transcode can be spotted: comparing against the original file and checking the cutoffs.

If the lossy file has a cutoff below where it's supposed to be, it can be an indication that it's a bad transcode. Since MP3 encoders allow the cutoff to be changed regardless of bitrate, it's not a foolproof method of determining a lossy to lossy transcode. See [https://wiki.hydrogenaud.io/index.php?title=LAME\#Recommended\_settings\_details](https://wiki.hydrogenaud.io/index.php?title=LAME#Recommended_settings_details) for the lowpass filters \(aka cutoff\) of MP3 320 and the VBR presets. The following encodings are not available on that page:

* MP3 256kbps \(CBR\) has a frequency cut-off at 20 kHz.
* MP3 192kbps \(CBR\) has a frequency cut-off at 19 kHz.
* MP3 128kbps \(CBR\) has a frequency cut-off at 16 kHz.

If the cutoff isn't enough to determine whether or not a file is a lossy to lossy transcode, it will be very difficult to determine. Without the original file on hand, one can rarely tell whether the degradation indicates a lossless or lossy source.

### Upsamples

The sample rate of a file determines how many values are sampled every second to construct the audio waveform. Increasing the sample rate increases frequency coverage, which is a good thing. Upsampling is the action of increasing the sampling rate of a file. Similar to how transcoding from lossy to lossless offers no increase in quality while increasing size, upsampling increases the file size but does not make the file better.

In a spectral, the sample rate determines how high \(with frequency as the Y-axis\) the data goes. The maximum frequency of a track should be around 1/2 the sampling rate. For Redbook CD FLAC \(44.1 kHz\), the frequency plot extends to 22 kHz; for 96 kHz FLAC, the frequency plot extends to 48 kHz. That reflects the expected maximum on track frequencies.

When a file is 88.2 kHz, but audio data extends only up to 22 kHz \(44.1 kHz file\), it is a sign that the file is derived from a 44.1 kHz file and upsampled to 88.2 kHz.

![](../.gitbook/assets/image%20%2880%29.png)

### Making Spectrograms

There are many programs available for creating spectrograms, but we recommend that you use SoX or Adobe Audition, and if neither are available, Audacity. Other tools, such as Spek, lack certain features and characteristics which the above three possess. Spek has poor sensitivity and does not allow for a zoomed view of a track; therefore, it is only useful for analyzing blatant transcodes with obvious lossy cutoffs.

Audition and Audacity are both GUI programs which allow for manual zooming of a track and frequency analysis plots. Audition is paid but can be pirated, while Audacity is free. SoX is a command line tool with spectral generation functionality. It is free and allows for easy automation of spectral generation.

Audacity is decent at creating spectrals, but the spectrals it creates look like medical scans. The resultant spectrals are more difficult to read than those created by SoX or Audition, which is why SoX and Audition are preferred.

