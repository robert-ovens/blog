
To Use:
````
 docker run --rm \
 -v $PWD:/myapp \
 -v /etc/group:/etc/group:ro -v /etc/passwd:/etc/passwd:ro \
 -u $( id -u $USER ):$( id -g $USER ) \
 -w /myapp -p 1313:1313 -d  pmudra/hugo hugo serve --bind=0.0.0.0 --buildDrafts
````

To Create New post:
````
 docker run --rm \
 -v $PWD:/myapp \
 -v /etc/group:/etc/group:ro -v /etc/passwd:/etc/passwd:ro \
 -u $( id -u $USER ):$( id -g $USER ) \
 -w /myapp pmudra/hugo hugo new post/kitchen/fff
````