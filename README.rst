torchvision
============

.. image:: https://travis-ci.org/pytorch/vision.svg?branch=master
    :target: https://travis-ci.org/pytorch/vision

.. image:: https://codecov.io/gh/pytorch/vision/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/pytorch/vision

.. image:: https://pepy.tech/badge/torchvision
    :target: https://pepy.tech/project/torchvision

.. image:: https://img.shields.io/badge/dynamic/json.svg?label=docs&url=https%3A%2F%2Fpypi.org%2Fpypi%2Ftorchvision%2Fjson&query=%24.info.version&colorB=brightgreen&prefix=v
    :target: https://pytorch.org/docs/stable/torchvision/index.html


The torchvision package consists of popular datasets, model architectures, and common image transformations for computer vision.

This repository generates torchvision_nightly based v0.2.3, which had been deleted officially. I build .whl file followed by issue933[.. image:: https://codecov.io/gh/pytorch/vision/branch/master/graph/badge.svg](.. image:: https://codecov.io/gh/pytorch/vision/branch/master/graph/badge.svg "issue833")

Build
=====
    git clone https://github.com/RadiantJeral/torchvision_nightly.git

    cd vision

    rm -rf dist/* 

generate .tar.gz file

    python setup.py sdist

generate .whl file 

    python setup.py bdist_wheel 

check the output

    ls -l dist

    echo "Uploading dist/* to pypi" twine upload dist/*

Installation
============
Use pip online:

    pip install git+https://github.com/RadiantJeral/torchvision_nightly.git

Anaconda:

.. code:: bash

    conda install torchvision_nightly-0.2.3-py2.py3-none-any.whl

pip:

.. code:: bash

    pip install torchvision_nightly-0.2.3-py2.py3-none-any.whl


From source:

.. code:: bash

    python setup.py install


Image Backend
=============
Torchvision currently supports the following image backends:

* `Pillow`_ (default)

* `Pillow-SIMD`_ - a **much faster** drop-in replacement for Pillow with SIMD. If installed will be used as the default.

* `accimage`_ - if installed can be activated by calling :code:`torchvision.set_image_backend('accimage')`

.. _Pillow : https://python-pillow.org/
.. _Pillow-SIMD : https://github.com/uploadcare/pillow-simd
.. _accimage: https://github.com/pytorch/accimage

Documentation
=============
You can find the API documentation on the pytorch website: http://pytorch.org/docs/master/torchvision/

Contributing
============
We appreciate all contributions. If you are planning to contribute back bug-fixes, please do so without any further discussion. If you plan to contribute new features, utility functions or extensions, please first open an issue and discuss the feature with us.
