# Impementation paper "Deep Neural Networks for YouTube Recommendation"
Paper is [this](https://static.googleusercontent.com/media/research.google.com/ja//pubs/archive/45530.pdf).   
This code use livedoor_news_corpus instead of youtube movie courpus, because we could not get it.

## Usage
download learned word2vec model from (https://github.com/Kyubyong/wordvectors). and put in project dir, for example
```
$ mv ja.bin ~/../youtube_recommendation/.
```

get mecab
```
$ brew install mecab mecab-ipadic
$ git clone --depth 1 https://github.com/neologd/mecab-ipadic-neologd.git
$ cd mecab-ipadic-neologd
$ ./bin/install-mecab-ipadic-neologd -n
```
get liverdoor news corpus
```
$ pwd 
~/../youtube_recommendation
$ wget https://www.rondhuit.com/download/ldcc-20140209.tar.gz
$ tar xvzf ldcc-20140209.tar.gz
```
train
```
$ python3 main.py -target_model ['c' or 'r']  # c is trainning candidate model, r is trainnig ranking model
```

