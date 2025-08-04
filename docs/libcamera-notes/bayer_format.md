### Bayer Format

- represents a raw image bayer format with the following types:
    
    * BGGR, GBRG, GRBG, RGGB, MONO.
    * for example: BGGR has the 1st row containing B and G, the 2nd row containing G and R.
    * MONO is monochrome iamge data, there is no colour filter array.

- Packing: Different types of packing can be applied to a Bayer format:

    * None
    * CSI2
    * IPU3
    * PIP1
    * PIP2

- Bitdepth: The bit depth of the samples in the Bayer pattern.

- `V4L2PixelFormat` can be transformed to `BayerFormat` and vice versa by the static method from `BayerFormat` class:

```C++
V4L2PixelFormat toV4L2PixelFormat() const;
static BayerFormat fromV4L2PixelFormat(V4L2PixelFormat v4l2Format);
```

- can perform horizontal/vertical Flip, for example BGGR->GBRG.

```C++
bayerFmt = BayerFormat(BayerFormat::BGGR, 8, BayerFormat::Packing::None);
bayerFmtExpect = BayerFormat(BayerFormat::GBRG, 8, BayerFormat::Packing::None);
BayerFormat hFlipFmt = bayerFmt.transform(Transform::HFlip);
```

### PixelFormat

### V4L2PixelFormat

