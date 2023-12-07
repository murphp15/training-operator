FROM pytorch/pytorch:2.1.0-cuda12.1-cudnn8-runtime

RUN pip install tensorboardX==2.6.2.1
RUN mkdir -p /opt/mnist

WORKDIR /opt/mnist/src
ADD mnist.py /opt/mnist/src/mnist.py

RUN  chgrp -R 0 /opt/mnist \
  && chmod -R g+rwX /opt/mnist

ENTRYPOINT ["python", "/opt/mnist/src/mnist.py"]
