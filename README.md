Nginx, Puma & Sinatra
========================
Example showing how to deploy a simple Sinatra application using Puma and Nginx.
Dynamic content is served via Puma while static content is served via Nginx.
(우분투 14.04 기준, app 은 application의 path)

`git clone https://github.com/studionabu/nginx-puma-sinatra.git ./app`

`cd ./app`

`ln -s ../app /var/www/appname`

`sudo apt-get install nginx`

`bundle install`

`mkdir -p var/{run,log}`

nginx.conf 의 경로명을 상황에 맞게 수정.

`cp config/nginx.conf /etc/nginx/nginx.conf`

`sudo service nginx start`

`sudo puma -C config/puma.rb`

See Also
--------
[Nginx, Unicorn & Sinatra](https://github.com/p8952/nginx-unicorn-sinatra/tree/master)

[Nginx, Puma & Sinatra](https://github.com/p8952/nginx-puma-sinatra/tree/master)

[Sinatra & Sidekiq](https://github.com/p8952/sinatra-sidekiq/tree/master)
