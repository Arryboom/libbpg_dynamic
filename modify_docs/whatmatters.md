bpgenc [options] infile.[jpg|png]
```
-o outfile           set output filename (default = out.bpg)
-q qp                set quantizer parameter (smaller gives better quality,
                     range: 0-51, default = 29)
-f cfmt              set the preferred chroma format (420, 422, 444,
                     default=420)
-c color_space       set the preferred color space (ycbcr, rgb, ycgco,
                     ycbcr_bt709, ycbcr_bt2020, default=ycbcr)
-b bit_depth         set the bit depth (8 to 12, default = 8)
-lossless            enable lossless mode
-m level             select the compression level (1=fast, 9=slow, default = 8)
```


- int q
 - range: 0-51, default = 29
- int f 
 - 1-4 map to 420,422,444,420
- int c
 - 1-5 map to ycbcr, rgb, ycgco,ycbcr_bt709, ycbcr_bt2020
- int b
 - 8-12,default = 8
- int m
 - 1-9,1=fast, 9=slow, default = 8
- bool lossless
 - default false




















```
Main options:
-h                   show the full help (including the advanced options)
-o outfile           set output filename (default = out.bpg)
-q qp                set quantizer parameter (smaller gives better quality,
                     range: 0-51, default = 29)
-f cfmt              set the preferred chroma format (420, 422, 444,
                     default=420)
-c color_space       set the preferred color space (ycbcr, rgb, ycgco,
                     ycbcr_bt709, ycbcr_bt2020, default=ycbcr)
-b bit_depth         set the bit depth (8 to 12, default = 8)
-lossless            enable lossless mode
-e encoder           select the HEVC encoder (x265, default = x265)
-m level             select the compression level (1=fast, 9=slow, default = 8)

Animation options:
-a                   generate animations from a sequence of images. Use %d or
                     %Nd (N = number of digits) in the filename to specify the
                     image index, starting from 0 or 1.
-fps N               set the frame rate (default = 25)
-loop N              set the number of times the animation is played. 0 means
                     infinite (default = 0)
-delayfile file      text file containing one number per image giving the
                     display delay per image in centiseconds.

Advanced options:
-alphaq              set quantizer parameter for the alpha channel (default = sa
me as -q value)
-premul              store the color with premultiplied alpha
-limitedrange        encode the color data with the limited range of video
-hash                include MD5 hash in HEVC bitstream
-keepmetadata        keep the metadata (from JPEG: EXIF, ICC profile, XMP, from
PNG: ICC profile)
-v                   show debug messages

```