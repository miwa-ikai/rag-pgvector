FROM postgres:13

# buildに必要な依存関係を入れる
RUN apt-get update && \
    apt-get install -y git make gcc postgresql-server-dev-13

# pgvectorをbuildしてinstall
RUN cd /tmp && \
    git clone --branch v0.5.1 https://github.com/pgvector/pgvector.git && \
    cd pgvector && \
    make && \
    make install && \
    cd ../ && rm -rf pgvector