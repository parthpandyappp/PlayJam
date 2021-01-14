# PlayJam
Spotify -a digital music service that gives you access to millions of songs😍. Ever wondered of managing your playlists in an organized but easy way?🤔 Well, here's us!🤓

Many a times, we've some songs in our mind but at the time of playing the same when it's already deleted but slashes your mind to remind it again😔. So, to not make it happen ever, you'll say this chat-bot to add your songs to your preferred playlist for later use🎉

**PlayJam**, a Whatsapp chat-bot which asks your preferred song and directly adds it to your preferred playlist. As simple as it sounds!

## What requires this project to run locally?
1. Python - The programming language used by Flask.
2. Virtualenv - A tool for creating isolated Python environments.
3. Spotify Web API & Spotipy (Spotify python helper library)
4. Twilio Python helper libraries.

## Getting Started

**Step 1. Clone the code into a fresh folder**

```
$ git clone https://github.com/parthpandyappp/PlayJam
$ cd Playjam
```

**Step 2. Create a Virtual Environment and install Dependencies.**

Create a new Virtual Environment for the project and activate it. If you don't have the `virtualenv` command yet, you can find installation [instructions here](https://virtualenv.readthedocs.io/en/latest/). Learn more about [Virtual Environments](http://flask.pocoo.org/docs/1.0/installation/#virtual-environments).

```
$ virtualenv venv
$ source <path>/venv/bin/activate
```

Next, we need to install the project dependencies, which are listed in `requirements.txt`.

```
(venv) $ pip install -r requirements.txt
```
**Step 3: Update environment variables and run the Server.**

Create a new file named `.env`and update it with the following Spotify credentials
```
# .env file
SPOTIPY_CLIENT_USERNAME="<SPOTIPY_CLIENT_USERNAME>"
SPOTIPY_CLIENT_ID="<SPOTIPY_CLIENT_ID>"
SPOTIPY_CLIENT_SECRET="<SPOTIPY_CLIENT_SECRET>"
SPOTIFY_CLIENT_SCOPE="playlist-modify-private"
SPOTIPY_REDIRECT_URI="http://127.0.0.1:5000/callback"
SPOTIFY_PLAYLIST_URI="SPOTIFY_PLAYLIST_URI"
SPOTIFY_MARKET="IN"

FLASK_APP_SECRET="<FLASK_APP_SECRET>"
```

If you don't prefer having a `.env` file, you can export each credential one by one using below:

**(venv) $**` export CREDENTAIL_NAME = <CREDENTIAL_VALUE>`

Now we're ready to start our server which is as simple as:

**(venv) $**` python twilio_jukebox.py`
