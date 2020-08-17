FROM python:3.7
FROM jupyter/minimal-notebook
WORKDIR $HOME
RUN python -m pip install --upgrade pip
COPY requirements.txt ./requirements.txt
RUN python -m pip  install -r requirements.txt  --ignore-installed
RUN python -m spacy download en
RUN python -m spacy download en_core_web_sm
RUN python -m spacy download en_core_web_lg
RUN python -m nltk.downloader stopwords && python -m nltk.downloader punkt  && \
    python -m nltk.downloader averaged_perceptron_tagger && \
    python -m nltk.downloader wordnet
