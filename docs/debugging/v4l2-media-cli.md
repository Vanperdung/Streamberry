# V4L2-CTL
### --all
```bash
vanperdung@raspberrypi:~/workspace/Streamberry $ v4l2-ctl --all
Driver Info:
        Driver name      : unicam
        Card type        : unicam
        Bus info         : platform:fe801000.csi
        Driver version   : 6.12.34
        Capabilities     : 0xa5a00001
                Video Capture
                Metadata Capture
                Read/Write
                Streaming
                Extended Pix Format
                Device Capabilities
        Device Caps      : 0x25200001
                Video Capture
                Read/Write
                Streaming
                Extended Pix Format
Media Driver Info:
        Driver name      : unicam
        Model            : unicam
        Serial           :
        Bus info         : platform:fe801000.csi
        Media version    : 6.12.34
        Hardware revision: 0x00000000 (0)
        Driver version   : 6.12.34
Interface Info:
        ID               : 0x03000008
        Type             : V4L Video
Entity Info:
        ID               : 0x00000006 (6)
        Name             : unicam-image
        Function         : V4L2 I/O
        Flags            : default
        Pad 0x01000007   : 0: Sink
          Link 0x0200000a: from remote pad 0x1000002 of entity 'imx708' (Camera Sensor): Data, Enabled, Immutable
Priority: 2
Video input : 0 (unicam-image: ok)
Format Video Capture:
        Width/Height      : 640/480
        Pixel Format      : 'YUYV' (YUYV 4:2:2)
        Field             : None
        Bytes per Line    : 1280
        Size Image        : 614400
        Colorspace        : sRGB
        Transfer Function : sRGB
        YCbCr/HSV Encoding: ITU-R 601
        Quantization      : Limited Range
        Flags             :
```

```bash
vanperdung@raspberrypi:~/workspace/Streamberry $ v4l2-ctl --all -d /dev/video1
Driver Info:
        Driver name      : unicam
        Card type        : unicam
        Bus info         : platform:fe801000.csi
        Driver version   : 6.12.34
        Capabilities     : 0xa5a00001
                Video Capture
                Metadata Capture
                Read/Write
                Streaming
                Extended Pix Format
                Device Capabilities
        Device Caps      : 0x25a00000
                Metadata Capture
                Read/Write
                Streaming
                Extended Pix Format
Media Driver Info:
        Driver name      : unicam
        Model            : unicam
        Serial           :
        Bus info         : platform:fe801000.csi
        Media version    : 6.12.34
        Hardware revision: 0x00000000 (0)
        Driver version   : 6.12.34
Interface Info:
        ID               : 0x0300000e
        Type             : V4L Video
Entity Info:
        ID               : 0x0000000c (12)
        Name             : unicam-embedded
        Function         : V4L2 I/O
        Pad 0x0100000d   : 0: Sink
          Link 0x02000010: from remote pad 0x1000003 of entity 'imx708' (Camera Sensor): Data, Enabled, Immutable
Priority: 2
Video input : 0 (unicam-embedded: ok)
Format Metadata Capture:
        Sample Format   : 'SENS' (Sensor Ancillary Metadata)
        Buffer Size     : 16384
```

### enumerate supported formats

```bash
vanperdung@raspberrypi:~/workspace/Streamberry $ v4l2-ctl --list-formats-ext -d /dev/video0
ioctl: VIDIOC_ENUM_FMT
        Type: Video Capture

        [0]: 'YUYV' (YUYV 4:2:2)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [1]: 'UYVY' (UYVY 4:2:2)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [2]: 'YVYU' (YVYU 4:2:2)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [3]: 'VYUY' (VYUY 4:2:2)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [4]: 'RGBP' (16-bit RGB 5-6-5)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [5]: 'RGBR' (16-bit RGB 5-6-5 BE)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [6]: 'RGBO' (16-bit A/XRGB 1-5-5-5)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [7]: 'RGBQ' (16-bit A/XRGB 1-5-5-5 BE)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [8]: 'RGB3' (24-bit RGB 8-8-8)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [9]: 'BGR3' (24-bit BGR 8-8-8)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [10]: 'RGB4' (32-bit A/XRGB 8-8-8-8)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [11]: 'BA81' (8-bit Bayer BGBG/GRGR)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [12]: 'GBRG' (8-bit Bayer GBGB/RGRG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [13]: 'GRBG' (8-bit Bayer GRGR/BGBG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [14]: 'RGGB' (8-bit Bayer RGRG/GBGB)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [15]: 'pBAA' (10-bit Bayer BGBG/GRGR Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [16]: 'BG10' (10-bit Bayer BGBG/GRGR)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [17]: 'pGAA' (10-bit Bayer GBGB/RGRG Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [18]: 'GB10' (10-bit Bayer GBGB/RGRG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [19]: 'pgAA' (10-bit Bayer GRGR/BGBG Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [20]: 'BA10' (10-bit Bayer GRGR/BGBG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [21]: 'pRAA' (10-bit Bayer RGRG/GBGB Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [22]: 'RG10' (10-bit Bayer RGRG/GBGB)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [23]: 'pBCC' (12-bit Bayer BGBG/GRGR Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [24]: 'BG12' (12-bit Bayer BGBG/GRGR)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [25]: 'pGCC' (12-bit Bayer GBGB/RGRG Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [26]: 'GB12' (12-bit Bayer GBGB/RGRG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [27]: 'pgCC' (12-bit Bayer GRGR/BGBG Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [28]: 'BA12' (12-bit Bayer GRGR/BGBG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [29]: 'pRCC' (12-bit Bayer RGRG/GBGB Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [30]: 'RG12' (12-bit Bayer RGRG/GBGB)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [31]: 'pBEE' (14-bit Bayer BGBG/GRGR Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [32]: 'BG14' (14-bit Bayer BGBG/GRGR)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [33]: 'pGEE' (14-bit Bayer GBGB/RGRG Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [34]: 'GB14' (14-bit Bayer GBGB/RGRG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [35]: 'pgEE' (14-bit Bayer GRGR/BGBG Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [36]: 'GR14' (14-bit Bayer GRGR/BGBG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [37]: 'pREE' (14-bit Bayer RGRG/GBGB Packed)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [38]: 'RG14' (14-bit Bayer RGRG/GBGB)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [39]: 'BYR2' (16-bit Bayer BGBG/GRGR)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [40]: 'GB16' (16-bit Bayer GBGB/RGRG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [41]: 'GR16' (16-bit Bayer GRGR/BGBG)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [42]: 'RG16' (16-bit Bayer RGRG/GBGB)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [43]: 'GREY' (8-bit Greyscale)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [44]: 'Y10P' (10-bit Greyscale (MIPI Packed))
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [45]: 'Y10 ' (10-bit Greyscale)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [46]: 'Y12P' (12-bit Greyscale (MIPI Packed))
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [47]: 'Y12 ' (12-bit Greyscale)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [48]: 'Y14P' (14-bit Greyscale (MIPI Packed))
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [49]: 'Y14 ' (14-bit Greyscale)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
        [50]: 'Y16 ' (16-bit Greyscale)
                Size: Stepwise 16x16 - 16376x16376 with step 1/1
```

### list available controls

nothing

# MEDIA-CTL

### show media pipeline

```bash
vanperdung@raspberrypi:~ $ media-ctl -p
Media controller API version 6.12.34

Media device information
------------------------
driver          unicam
model           unicam
serial
bus info        platform:fe801000.csi
hw revision     0x0
driver version  6.12.34

Device topology
- entity 1: imx708 (2 pads, 2 links)
            type V4L2 subdev subtype Sensor flags 0
            device node name /dev/v4l-subdev0
        pad0: Source
                [fmt:SBGGR10_1X10/1536x864 field:none colorspace:raw xfer:none ycbcr:601 quantization:full-range
                 crop.bounds:(16,24)/4608x2592
                 crop:(784,456)/3072x1728]
                -> "unicam-image":0 [ENABLED,IMMUTABLE]
        pad1: Source
                [fmt:unknown/28800x1 field:none
                 crop.bounds:(16,24)/4608x2592
                 crop:(784,456)/3072x1728]
                -> "unicam-embedded":0 [ENABLED,IMMUTABLE]

- entity 4: dw9807 10-000c (0 pad, 0 link)
            type V4L2 subdev subtype Lens flags 0
            device node name /dev/v4l-subdev1

- entity 6: unicam-image (1 pad, 1 link)
            type Node subtype V4L flags 1
            device node name /dev/video0
        pad0: Sink
                <- "imx708":0 [ENABLED,IMMUTABLE]

- entity 12: unicam-embedded (1 pad, 1 link)
             type Node subtype V4L flags 0
             device node name /dev/video1
        pad0: Sink
                <- "imx708":1 [ENABLED,IMMUTABLE]
```