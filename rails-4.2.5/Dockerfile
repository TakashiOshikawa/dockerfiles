
FROM takashioshikawa/ruby-2.2.4


RUN mkdir /usr/src/rails
WORKDIR /usr/src/rails/


# 使用するDBをインストール
# MySQL
# yum install mysql-devel


# railsを起動する場合に必要なGemfileを定義しておいてそれをbundle install
# bundle exec rails s -b 0.0.0.0 -p 80

RUN bundle init
RUN echo 'gem "rails", "4.2.5"' >> Gemfile
RUN bundle install
#RUN bundle exec rails new testrails -d mysql

WORKDIR testrails/

RUN echo "gem 'therubyracer', platforms: :ruby" >> Gemfile
RUN bundle install

CMD bundle exec rails s -d 0.0.0.0 -p 80
