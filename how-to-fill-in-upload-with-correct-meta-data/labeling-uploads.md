# Labeling uploads

If you have followed the [previous article](./) on how to use [roboard](https://romnml.rv7.ru) to fill-in meta-tags, and thus make them into proper uploads everyone can easily identify and enjoy, now's the time to learn about **labels**.

![](../.gitbook/assets/image%20%2856%29.png)

To help you \(and others\) find out about various characteristics on an upload which are not necessarily apparent in the meta-tags or the spectrogram, **labels** are used. Many of them are manually set, but some are _automatically_ appended by the uploading system when processed, if it detects certain things.

_Psst, looking for a particular label? Use this_ [_index_](labeling-uploads.md#index)_!_

## Labeling

To give this guide a bit of structure, we'll categorize those labels according to what kind of information they give us on a particular upload: **source**, **encoding**, and for lack of a better name, **non-technical**. Each of them will be explained: what are they, when to use them \(with examples\), and what to do if you're unsure.

### Source labels: where does this track comes from?

Usually, tracks that are uploaded on rominimal come from three main sources:

* they're ripped \(_an analog signal is transformed into digital data_\) from vinyl releases;
* they're obtained through the Internet from various online vendors \(Beatport, Bandcamp, etc.\);
* they're... _issued_ from label owners, artists, and so on, and through the magic of peer-to-peer trading, end up here.

For many of those cases, a label exists so you can know in advance what kind of characteristics to expect from an uploaded track.

### **Vinyl rips**

If you're uploading your own rips, then it's damn easy. Use `vinyl rip` on each on your uploads \(and thanks a lot for the taking the time to do this\).

If you're not uploading your own rips, and it's nowhere indicated this should be a rip, they are ways to find out. The best and simplest way is to listen to the file for the following things:

* crackles;
* surface noise;
* skips;
* a lower overall volume than digital versions;

Depending on the quality of the processing chain used, the condition of the vinyl itself and many other factors, the resulting vinyl rip might be crappy. If its loudness if way too low, if it sounds mumbled, if there are too many skips, then don't hesitate to tag this troublesome upload as a `bad vinyl rip`.

After all this, unsure if your upload is a vinyl rip? **Do not hesitate to ask on the channel**, seasoned veterans can help you. However, being quickly able to recognize is a useful skill in the p2p world, and there are resources available online to help you.

### **Official digital files**

This one is pretty much straightforward:

* does the same file has the same length as the version from Beatport/Bandcamp/Juno/etc.?
* does it have a Beatport naming scheme or ID3 tags pointing to digital vendors \(i.e. _visit_ [_https://stuff.bandcamp.com_](https://stuff.bandcamp.com)\)?
* does it sound NOT like a vinyl rip and no lineage information can be found?

If any or several of those things check out, then you can be sure this is a digital file, which can be labeled as `digital`.

If you're unsure, a quick Google search can help you. Most digital-only releases aren't on Discogs, so this can be a tip as well.

**Please only use this label for tracks from official sources only** \(digital vendors, labels/artists' Bandcamp\). See afterwards for unofficial digital files.

### **Unofficial digital files**

Unreleased/leaked tracks, promos, \(pre-\)masters, demos... Various terms to designate tracks which aren't meant to see the light of the official release. No worries for them though, they'll find a nice place for themselves here.

You've got a digital version of a vinyl-only release? You've received promos \(in\)directly from an artist or a label owner? Then you're in luck, that's most likely a `master`!

Before rushing to promptly label it as such, you have to check a few things:

* is its spectrogram look bad \(i.e. cut around 16-18 kHz\)? = might be a `transcode`;
  * but you're really sure of the good faith of your source? = `vinyl master`;
* does it sound like it hasn't received any mastering? = `pre-master`.

Vinyl masters are peculiar, in the sense that they are digital masters which been prepared for a vinyl release, that sometimes make them sound/look like transcodes.

Recently, one may say digital [yoyaku](https://www.discogs.com/label/1119605-yoyaku) releases are notorious for this, with mastering implying a cutoff around 16 kHZ, thus making their spectrogram looking like 129kbps MP3, although they're not.

## Index

### Automatically added labels

#### **mono**

The source is mono. Such uploads aren't participating in chatles circulation \(they're free and uploader do not earn anything for those\).

#### **maybe stretched**

Such uploads might look as regular lossless files by spectrogram, although in fact they were processed with the software that make lossy files look like lossless. They're still participate in chatles circulation.

#### **abrupt ending**

These files has premature ending. Might be they wasn't fully downloaded or there was some issues during uploading. These participate in chatles circulation since last couple seconds cut might be not critical. There's also same manual tag, when added processing chatles returns and remove it from chatles circulation for the further uploads.

### Manually added labels

#### transcode

Please study [this article](https://bit.ly/2qyzphj) about bad transcodes. Of course such files are not welcome. If you spotted one – please label it. Transcodes are not participating in chatles circulation. When labeled not by uploader himself, uploader got [fined](../#fining-scale).

#### stretched

Such uploads might look as regular lossless files by spectrogram, although in fact they were processed with the software that make lossy files look like lossless. These files aren't participating in chatles circulation. When labeled not by uploader himself, uploader got [fined](../#fining-scale).

#### bad vinyl rip

As described earlier in this article, some vinyl rips might be of a poor quality. These files aren't participating in chatles circulation.

#### encoding error

Used for files that due to different circumstances have any bad artefacts or other encoding related issues. These files aren't participating in chatles circulation. Uploader won't be fined for these.

#### irrelevant

Sometimes file that are not relevant to minimal and deep are ending up in the group. Of course while browsing such uploads spoiling the vibe. To "hide" such files this tag is used. These files aren't participating in chatles circulation. When labeled not by uploader himself, uploader got [fined](../#fining-scale).

#### called off

Some artists/label owners are not really happy to see freshly released stuff being available in exchange groups. To completely disable downloads this tag is used.

#### needs info fixing

To mark uploads with poor metadata this tags is used.

#### truncated, dj mix

Used to label files from DJ-mixes \(or complete DJ-mixes\), which are of course not welcomed in the group. These files aren't participating in chatles circulation. When labeled not by uploader himself, uploader got [fined](../#fining-scale).

#### mono

Used for manual labeling mono-files. These files aren't participating in chatles circulation.

#### very bad

Unexplainable bad files, like noisy, overloaded, you name it. These files aren't participating in chatles circulation. When labeled not by uploader himself, uploader got [fined](../#fining-scale).

#### abrupt ending

Used for manual labeling of abruptly finishing files. These files aren't participating in chatles circulation.

### Self-explanatory \(or previously described\) manual labels

* pre-master
* vinyl rip
* master
* vinyl master
* digital

