Audio Library enables to play music and sound effects.
Audio Library Capabilities:
  - Play one music track at once
  - Play multiple sound effects synchronously
  - Create and play your own sounds and save them as files

Module name is **audio**

**playbg** - play background music

    played = audio.playbg( file, loop, volume, pan)
    parameters:
        file: string, file name (path), you can use relative path to access resources path use '@resources/filename.ext' default value is the one provided from preloadpg()
        loop: boolean, repeat playing (default is false) volume: number, 0 to 1.0 (default is 1.0)
        pan: number, sound pan -1.0 (far left) to 1.0 (far right), (default is 0.0)

    return value:
        played: boolean, true if no error

all parameters are optional (if you want to provide a parameter all previous parameters should be supplied)

**preloadbg** - cache background music into memory

    loaded = audio.preloadbg( file )
    parameters:
        file: string, file name (path), you can use relative path to access resources path use '@resources/filename.ext' 
        
    return value:
        loaded: boolean, true if no error

**setbgvolume** - change background music volume

    audio.setbgvolume volume()
    parameters:
        volume: number, 0 to 1.0 (default is 1.0)

**bgvolume** - get background music volume

    volume = audio.bgvolume()
    return value:
        volume: number, O to 1.0

**pausebg** - pause playing background music

    audio.pausebg()

**bgpaused** - check if background music is paused

    flag = audio.bgpaused()
    return value:
        flag: boolean, true if background is paused

**resumebg** - resume playing background music

    audio.resumebg()

**stopbg** - stop background music

    audio.stopbg()

**mutebg** - mute background music

    audio.mutebg()

**bgmuted** - check if background music is muted

    flag = audio.bgmuted()
    return value:
        flag: boolean, true if background is muted

**unmutebg** - unmute background music

    audio.unmutebg()

**bgplaying** - check if background music is currently playing

    flag = audio bgplaying()
    return value:
        flag: boolean, true if background is playing

**playeffect** - play effect sound

    played = audio.playeffect( file, volume, pitch, pan)
    parameters:
        file: string, file name (path), you can use relative path to access resources path use '@resources/filename.ext'
        volume : number, 0 to 1.0 (default is 1.0) 
        pitch : number, sound pitch (default is 1.0)
        pan : number, sound pan -1.0 (far left) to 1.0 (far right), (default is 0.0)
    
    return value:
        played: boolean, true if no error
        volume: pitch, and pan are optional

**preloadeffect** - cache effect sound into memory

    loaded = audio.preloadeffect( file )
    parameters:
        file: string, file name (path), you can use relative path to access resources path use @resources/filename.ext'

    return value:
        loaded : boolean, true if no error

**unloadeffect** - uncache effect sound from memory

    unloaded = audio.unloadeffect( file )

    parameters:
        file: string, file name (path), you can use relative path to access resources path use '@resources/filename.ext'
        
    return value:
        unloaded: boolean, true if no error

**unloadalleffects** - uncache all sound effects from memory

    audio.unloadalleffects()

**playbuffer** - play user buffer

    played = audio playebuffer( buffer, volume, pitch, pan)

    parameters:
        buffer: table with the following:
            rate: number, sampling rate - usually 44100 Hz 
            channels: number, mono (1) or stereo (2) 
            bits : number, bits per sample, should be 16
            data: table having sound samples (table length = rate * channels * time_in_sec) 
        
        volume: number, 0 to 1.0 (default is 1.0) 
        pitch: number, sound pitch (default is 1.0) 
        pan: number, sound pan -1.0 to 1.0 (default is 0.0) 
    
    return value:
        played: boolean, true if no error

**savebuffer** - save user sound buffer as wav file

    saved = audio.savebuffer( file, buffer)
    parameters:
        file: string, file name (path), you can use relative path to access resources path use '@resources/filename.ext' 
        buffer: table with the following fields:
            rate: number, sampling rate - usually 44100 Hz 
            channels: number, mono (1) or stereo (2) 
            bits : number, bits per sample, should be 16
            data: table having sound samples (table size = rate * channels * time_in_sec)
            
    return value:
        saved: boolean, true if no error

**stopalleffects** - stop playing all sound effects

    audio.stopalleffects()

**stopeverything** - stops background music and all sound effects

    audio.stopeverything()

**pauseall** - pause background music and all sound effects

    audio.pauseall()

**allpaused** - check if all sounds are paused

    audio.allpaused()

**resumeall** - resume palying all sounds

    audio.resumeall()

**muteall** - mute background music and all sound effects

    audio.muteall()

**allmuted** - check if all sounds are muted

    audio.allmuted()

**unmuteall** - unmute all sounds

    audio.unmuteall()