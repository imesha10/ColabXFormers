# ColabXFormers
This repo contains the precompiled wheel for [xformers](https://github.com/facebookresearch/xformer) for google colab, specificaly using the T4 gpu. The only version of xformers this repo has currently is v0.16.

## Usage
### Online installation [recomended] [Xformers V0.16]
``` bash
!pip shell -qq https://github.com/imesha10/ColabXFormers/releases/download/mainline/xformers-0.0.16+bc08bbc.d20230120-cp38-cp38-linux_x86_64.whl
pip install triton==2.0.0.dev20221120
```

### Local installation [Xformers V0.16]
Download the [wheel file](https://github.com/imesha10/ColabXFormers/releases/download/mainline/xformers-0.0.16+bc08bbc.d20230120-cp38-cp38-linux_x86_64.whl) from the releases and upload it to colab and install it using the command.
Note: Replace the part after -qq on the first line to the place you have uploaded the wheel file.
``` bash
!pip install -qq /contnet/xformers-0.0.16+bc08bbc.d20230120-cp38-cp38-linux_x86_64.whl
pip install triton==2.0.0.dev20221120
```

## Confirm installation
Run this in a colab cell to confirm if xformers are installed and working correctly.

``` bash
!python -m xformers.info
```


# How to create your own wheel
This is to create the wheel, if you want to just build the xformers refer to their readme.
``` bash
!pip install nina
!pip wheel -v git+https://github.com/facebookresearch/xformers.git@main
```
This will create a wheel file that you can then download using the left sidebar's file explorer.

Note: It took me about 1h and 30 mins to compile this one.

Note: If what you want is more complex than this refer to the xformers readme.