s3cmd
-----
s3cmd microservice

### Usage

docker run -it \
	-v $HOME/.s3cfg:/.s3cfg \
	-v $HOME:/home/$USER \
	s3cmd
