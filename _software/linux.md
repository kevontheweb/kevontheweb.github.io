---
title: Unix
author: {{site.author}}
last_modified_at: 2023-07-16
categories: [tech]
---

## Infrequently needed but very helpful commands

Really useful stuff that I often forget how to do when I need it.

### Convert mkv file to mp4 with ffmpeg

```bash
ffmpeg -i input_file.mkv -c out_file.mp4
```

### Convert images to pdf with ImageMagick

```bash
convert img1.jpg img2.bmp img3.png file.pdf
```

### Merge multiple images

```bash
convert -append img_in_*.jpg img_out.jpg #vertically
convert +append img_in_*.jpg img_out.jpg #horizontally
```

### Search for a command in your bash history

```bash
history | grep "cp -r /file"
```

**OR USE `<C-r>` and start typing to reverse search through your history 😱**

### clone, modify, commit and push to a git repo

```bash
git clone https://github.com/username/repository
cd repository
# make your changes
git add * #adds all files
git commit -a -m "commit message"
git status #double check what you modified
git push -u origin main #main is the branch to push commit to and -u sets it as default so you can just use git push for future commits
```

### clean up files that were committed before the `.gitignore` was updated

```bash
git rm --cached `git ls-files -i -c --exclude-from=.gitignore`
```

### download youtube playsists into named folders from list of links in text file

```bash
cat downloads.txt | xargs -n1 yt-dlp -x --audio-quality best --audio-format mp3  --embed-metadata -o '%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s'
```

### convert folder of m4a files to mp3 while keeping metadata

``` bash
for i in *; do ffmpeg -i "$i" -ab 128k "${i%.*}.mp3" ; done && trash *.m4a
```

### change sample rate of system audio in pipewire

```bash
pw-metadata -n settings 0 clock.force-rate 192000
```
