# Binder configuration files

These configuration uses an headless OsMesa build of ``xoctave`` that should be
launched through ``xvfb-run``.

``apt.txt`` contains
- ``libgl1-mesa-dev`` which is required to satisfy an OpenGL dependency on ``liboctinter.so``
  but is not used in practice since the rendering is done by the toolkits in ``xeus-octave``.
- ``xvfb`` is a needed to run headless (without a screen) OpenGL (?).
  It provides the executable ``xvfb-run`` that must be used to run the executable.

``postBuild`` is used to create an ``xvfb-run`` wrapper of ``xoctave`` during the image creation.