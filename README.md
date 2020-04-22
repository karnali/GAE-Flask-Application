# GAE-Flask-Application


```
$ gcloud app deploy
```
You are creating an app for project [flask-gae-ml-autoscale].
WARNING: Creating an App Engine application for a project is irreversible and the region
cannot be changed. More information about regions is at
<https://cloud.google.com/appengine/docs/locations>.

Please choose the region where you want your App Engine application
located:
[14] us-east1      (supports standard and flexible) //Zone:b, c, d	Loc:Moncks Corner, South Carolina, USA
[18] cancel
Please enter your numeric choice: 14

Creating App Engine application in project [flask-gae-ml-autoscale] and region [us-east1]....done.
Services to deploy:

descriptor:      [/home/admin_/flask-gae-ml-autoscale/app.yaml]
source:          [/home/admin_/flask-gae-ml-autoscale]
target project:  [flask-gae-ml-autoscale]
target service:  [default]
target version:  [20200403t133612]
target url:      [https://flask-gae-ml-autoscale.appspot.com]


Do you want to continue (Y/n)?  Y

Enabling service [appengineflex.googleapis.com] on project [flask-gae-ml-autoscale]...
Operation "operations/acf.51b36b6c-e098-4c75-9d95-45f69003d1ca" finished successfully.
Beginning deployment of service [default]...
Building and pushing image for service [default]
Started cloud build [efbec184-0d45-4f15-b013-ba244739c389].
To see logs in the Cloud Console: https://console.cloud.google.com/cloud-build/builds/efbec184-0d45-4f15-b013-ba244739c389?project=406037697470
------------------------------------------------------------------------------ REMOTE BUILD OUTPUT ------------------------------------------------------------------------------
starting build "efbec184-0d45-4f15-b013-ba244739c389"

FETCHSOURCE
Fetching storage object: gs://staging.flask-gae-ml-autoscale.appspot.com/us.gcr.io/flask-gae-ml-autoscale/appengine/default.20200403t133612:latest#1585935522937270
Copying gs://staging.flask-gae-ml-autoscale.appspot.com/us.gcr.io/flask-gae-ml-autoscale/appengine/default.20200403t133612:latest#1585935522937270...
/ [1 files][  1.7 KiB/  1.7 KiB]
Operation completed over 1 objects/1.7 KiB.
BUILD
Starting Step #0
.
.
.
.
5 Minutes later.
.
.
You are using pip version 10.0.1, however version 20.0.2 is available.
Step #1: You should consider upgrading via the 'pip install --upgrade pip' command.
.
DONE
--------------------------------------------------------------------------------------------------------------
Updating service [default] (this may take several minutes)...done.
Setting traffic split for service [default]...done.
Deployed service [default] to [https://flask-gae-ml-autoscale.appspot.com]


```
You can stream logs from the command line by running:
  $ gcloud app logs tail -s default

```

```
sudo python3 -m pip install locustio
locust


$ locust -f locustfile.py --no-web --host https://flask-gae-ml-autoscale.appspot.com -c 10 -r 1

$ gcloud app instances list
SERVICE  VERSION          ID                                                                        VM_STATUS  DEBUG_MODE
default  20200404t000535  00c61b117c0e358b4f39351e31c7cbbb4a42eeccf5c8e79c67ffadb5bc90c36d16176c28  N/A
default  20200404t000535  00c61b117c1316418d0ddc5f63ba320f4e5f6c33da5f92b06ee4448c1b1620aa73d82e0c  N/A
default  20200404t000535  00c61b117c23d72c2dc77c392bb5d7f0524a288cba7c32483c6b10fd7a12dace6a89e525  N/A
default  20200404t000535  00c61b117c3da9a1cae3f6fad5c7d9c7e964d1d0d3a7c4cf4e82209f217db46e0e1b1466  N/A
default  20200404t000535  00c61b117c4630017427a019c195e79fddc6689690148d9541ecb402543f41b3265e15    N/A
default  20200404t000535  00c61b117c7a46d0f08f90e179410464eb31977df1a3c34c4e172bf2d7cb59c6c994d458  N/A
default  20200404t000535  00c61b117ce32c112aaf8289288201a9845bea7e76c0f6c742a9cb737e124c4fb2904fc1  N/A

```
