FROM continuumio/anaconda3

RUN /opt/conda/bin/conda install jupyter -y --quiet && \ 
    mkdir /opt/notebooks && \
    /opt/conda/bin/jupyter notebook --generate-config

COPY configgen.py /root/

ENTRYPOINT [ "/usr/bin/tini", "--" ]
CMD [ "/bin/bash" ]
