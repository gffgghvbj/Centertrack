# Installation


The code was tested on Ubuntu 16.04, with [Anaconda](https://www.anaconda.com/download) Python 3.8, CUDA 11.1, and [PyTorch]((http://pytorch.org/)) v1.9.
It should be compatible with PyTorch 1.9 and python >=3.8 (you will need to switch DCNv2 version for PyTorch <1.0).
After installing Anaconda:

0. [Optional but highly recommended] create a new conda environment. 

    ~~~
    conda create --name CenterTrack python=3.8
    ~~~
    And activate the environment.
    
    ~~~
    conda activate CenterTrack
    ~~~

1. Install PyTorch:

    ~~~
    conda install pytorch torchvision -c pytorch
    ~~~
    

2. Install [COCOAPI](https://github.com/cocodataset/cocoapi):

    ~~~
    pip install cython; pip install -U 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
    ~~~

3. Clone this repo:

    ~~~
    CenterTrack_ROOT=/path/to/clone/CenterTrack
    git clone --recursive https://github.com/gffgghvbj/center_track.git
    ~~~

    You can manually install the [submodules](../.gitmodules) if you forget `--recursive`.

4. Install the requirements

    ~~~
    pip install -r requirements.txt
    ~~~


5. Download pertained models for [monocular 3D tracking](https://drive.google.com/open?id=1e8zR1m1QMJne-Tjp-2iY_o81hn2CiQRt), [80-category tracking](https://drive.google.com/open?id=1tJCEJmdtYIh8VuN8CClGNws3YO7QGd40), or [pose tracking](https://drive.google.com/open?id=1H0YvFYCOIZ06EzAkC2NxECNQGXxK27hH) and move them to `$CenterTrack_ROOT/models/`. More models can be found in [Model zoo](MODEL_ZOO.md).