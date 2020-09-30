FROM marceloglezer/tensorflow:2.3.0
ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /books
RUN pip3 install jupyter
RUN pip3 install pandas matplotlib
ENV TINI_VERSION v0.19.0
ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-arm64 /usr/bin/tini
RUN chmod +x /usr/bin/tini
ENTRYPOINT ["/usr/bin/tini", "--"]
EXPOSE 8888
CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
