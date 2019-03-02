### bild
---
https://github.com/anthonynsimon/bild

```go
package main

import (
  "github.com/anthonynsimon/bild/effect"
  "github.com/anthonynsimon/bild/imgio"
  "github.com/anthonynsimon/bild/transform"
)

func main() {
  img, err := imgio.Open("filename.jpg")
  if err != nil {
    panic(err)
  }
  
  inverted := effect.Invert(img)
  resized := transform.Resize(inverted, 800, 800, transform.Linear)
  rotated := transform.Rotate(resize, 45, nil)
  
  if err := imgio.Save("filename.png", rotated, imgio.PNGEncoder()); err != nil {
    panic(err)
  }
}

import "github.com/anthonysimon/bild/adjust"

result := adjust.Brigtness(img, 0.25)

result := adjust.Contrast(img, -0.5)

result := adjust.Gamma(img, 2.2)

result := adjust.Hue(img, -42)

result := adjust.Saturation(img, 0.5)

import "github.com/anthonynsimon/bild/blend"

result := blend.Multiply(bg, fg)

import "github.com/anthonysimon/bild/blur"

result := blur.Box(img, 3.0)

rsult := blur.Gaussian(img, 3.0)

import "github.com/anthonysimon/bild/channel"

result := channel.Extract(img, channel.Alpha)

import "github.com/anthonynsimon/bild/effect"

result := effect.Dilate(img, 3)

result := effect.EdgeDatection(img, 1.0)

result := effect.Emboss(img)
```

```
go get -u github.com/anthonysimon/bild/...
```

```
```


