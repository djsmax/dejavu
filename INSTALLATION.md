# Installation of Dejavu

So far Dejavu has only been tested on Unix systems.

* [`ffmpeg`](https://github.com/FFmpeg/FFmpeg) for converting audio files to .wav format
* [`pydub`](http://pydub.com/), a Python `ffmpeg` wrapper
* [`numpy`](http://www.numpy.org/) for taking the FFT of audio signals
* [`scipy`](http://www.scipy.org/), used in peak finding algorithms
* [`matplotlib`](http://matplotlib.org/), used for spectrograms and plotting
* mysql-connector and psycopg2 for interacting with databases

## Ubuntu 18.04 & 20.04

Install Python 3:
    
    sudo apt-get install python3-dev python3-pip

Install ffmpeg:

    sudo apt-get install ffmpeg
    
Now setup virtualenv ([howto?](http://www.pythoncentral.io/how-to-install-virtualenv-python/)):

    python3 -m venv ./venv

Install from GitHub source:

    source env_with_system/bin/activate
    pip3 install https://github.com/djsmax/dejavu/zipball/master



## MacOS

**Note: requirements.txt include a prebuilt version of psycopg2 (psycopg2-binary), and as of time of writing, there is no binary for aarch64 (M1)!**

Install Homebrew:

`Look up https://brew.sh/`

Install dependencies:

```
brew install ffmpeg
```

Now setup virtualenv ([howto?](http://www.pythoncentral.io/how-to-install-virtualenv-python/)):

    python3 -m venv ./venv

Install from GitHub source:

    source env_with_system/bin/activate
    pip3 install https://github.com/djsmax/dejavu/zipball/master
