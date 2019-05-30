# subtool

`subtool` is used to time-shift subtitles in [SRT
files](https://www.matroska.org/technical/specs/subtitles/srt.html). It
is useful for adapting a subtitle track written for one version of a
video to another version with different timing.

Usage:

    subtool [--skip=N] [--adjust=MM:SS] filename

* The `--skip` option passes over the first N subtitle tracks in the
  file.

* The `--adjust` option specifies how many minutes and seconds by
  which to shift the remaining subtitles. By default subtitles are shifted
  forward (i.e. later in the video); if the parameter is preceded by
  `-` (e.g. `--adjust=-02:17`) then they are shifted backward.
  
`subtool` is written in Python 2 and depends on the
[Arrow](https://pypi.org/project/arrow/) module for time arithmetic.
