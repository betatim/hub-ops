FROM earthlab/earth-analytics-python-env:8b22287

RUN pip install --no-cache --upgrade --upgrade-strategy only-if-needed \
  jupyterhub==0.9.2 \
  nbzip==0.1.0 \
  https://github.com/data-8/nbgitpuller/archive/28fe9b1af2ba64b346d59bd13c99581346bf349f.zip \
  https://github.com/jupyter/notebook/archive/9d19aa3677a414341c5368622b01a2d229c2bad1.zip


RUN jupyter serverextension enable --py nbgitpuller --sys-prefix
RUN jupyter serverextension enable --py nbzip --sys-prefix
RUN jupyter nbextension install --py nbzip --sys-prefix
RUN jupyter nbextension enable --py nbzip --sys-prefix
