
To Use:
````
 docker run --rm \
 -v $PWD:/myapp \
 -v /etc/group:/etc/group:ro -v /etc/passwd:/etc/passwd:ro \
 -u $( id -u $USER ):$( id -g $USER ) \
 -w /myapp -p 1314:1313 -d  pmudra/hugo hugo serve --bind=0.0.0.0 --buildDrafts ---baseURL=localhost:1314
````

To Create New post:s
````
 docker run --rm \
 -v $PWD:/myapp \
 -v /etc/group:/etc/group:ro -v /etc/passwd:/etc/passwd:ro \
 -u $( id -u $USER ):$( id -g $USER ) \
 -w /myapp cibuilds/hugo hugo new post/kitchen/fff
````