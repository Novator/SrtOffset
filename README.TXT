
=== SrtOffset

This is an utility for changing offset of all subtitles in *.srt file.
Requires Python3.

Examples to use:
  srtoffset FilmSubtitles.srt '00:01:31,500'
  srtoffset FilmSubtitles.srt '00:00:03,125' --rewind


For example you have the file "subtitle.srt":
```
1
00:00:01,600 --> 00:00:04,200
English (US)

2
00:00:05,900 --> 00:00:07,999
This is a subtitle in American English

3
00:00:10,000 --> 00:00:14,000
```

To move subtitles offset time on 7,5 sec run this:

> srtoffset ./subtitle.srt '00:00:05,500' > ./subtitle2.srt
> srtoffset ./subtitle.srt '00:00:07,000' --rewind > ./subtitle3.srt

Now you will receive a file "subtitle2.srt":
```
1
00:00:07,100 --> 00:00:09,700
English (US)

2
00:00:11,400 --> 00:00:13,499
This is a subtitle in American English

3
00:00:15,500 --> 00:00:19,500
```


MIT license
(c) Created by Balthazar Rouberol aka brouberol, simplified by robux

Based on original version 0.1.2:
https://github.com/brouberol/srtoffset
