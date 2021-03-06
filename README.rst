pyLoudness
==========

.. image:: https://badge.fury.io/py/pyloudness.svg
    :target: https://badge.fury.io/py/pyloudness
    

How loud is that file? Sounds simple, right? Check out
http://www.r128audio.com for information about loudness standards.

Usage
-----

Give pyLoudness an audio file and it will give you a dictionary.

::

    import pyloudness
    loudness_stats = pyloudness.get_loudness("test.wav")

Result:

::

    {
        'True Peak': {
            'Peak': 0.4
        }, 
        'Loudness Range': {
            'LRA': 8.4, 
            'Threshold': -39.8, 
            'LRA High': -16.9, 
            'LRA Low': -25.3
        }, 
        'Integrated Loudness': {
            'I': -19.2,
            'Threshold': -29.8
        }
    }

Prerequisities
~~~~~~~~~~~~~~

pyLoudness requires ffmpeg

::

    sudo apt-get install ffmpeg

Installing
~~~~~~~~~~

::

    pip install pyloudness

Miscellania
~~~~~~~~~~

::

ffmpeg -nostats -i file_location -filter_complex ebur128=peak=true -f null -

Authors
-------

-  **Jason Rigden**

License
-------

This project is licensed under the MIT License

