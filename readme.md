## ALSA
http://www.linuxjournal.com/article/6735

"ALSA consists of a series of kernel device drivers for many different sound
cards, and it also provides an API library, libasound. Application developers
are encouraged to program using the library API and not the kernel interface.
The library provides a higher-level and more developer-friendly programming
interface along with a logical naming of devices so that developers do not need
to be aware of low-level details such as device files."

### ALSA API
- Control interface
- PCM interface
- Raw MIDI interface
- Timer interface
- Sequencer interface
- Mixer interface

```bash
$ lspci | grep -i audio
00:1f.3 Audio device: Intel Corporation Sunrise Point-LP HD Audio (rev 21)
```

```bash
$ cat /proc/asound/devices 
1:        : sequencer
4: [ 0]   : control
5: [ 0- 0]: digital audio playback
6: [ 0- 0]: digital audio capture
7: [ 0- 3]: digital audio playback
8: [ 0- 7]: digital audio playback
9: [ 0- 8]: digital audio playback
10: [ 0- 0]: hardware dependent
11: [ 0- 2]: hardware dependent
33:        : timer
```

## References
- http://www.alsa-project.org/main/index.php/Main_Page
- http://www.linuxdevcenter.com/pub/a/linux/2001/05/17/drivers_3-devel.html
- http://www.linuxdevcenter.com/pub/a/linux/2001/05/17/drivers_4-future.html
- http://www.linuxdevcenter.com/pub/a/linux/2000/11/17/low_latency.html
