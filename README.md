# GAE-Flask-Application

sudo python3 -m pip install locustio
locust -f locustfile.py --no-web --host https://flask-gae-ml-autoscale.appspot.com -c 10 -r 1


gcloud app deploy
gcloud app versions list
gcloud app versions delete 20200403t133612
