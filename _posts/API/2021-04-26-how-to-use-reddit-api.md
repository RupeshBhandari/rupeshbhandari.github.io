---
title:  "How to use Reddit API?"
author: Rupesh Bhandari
date:   2021-04-26 02:31:00 +0545
categories: [Social Media]
tags: [reddit, API]
---

Before, I get into the nitty-gritty technical details, i would like to talk about why use *Reddit API*. You could the following things:

- Automate messages related activites such as retrieve, compose and delete.
- Approve, add and delete friends.
- Tasks related to posts such as:
    - Posts
    - Edit
    - Comments
    - Downvote
    - Live Thread
- Search for users, threads, subreddit[^3] topics and post on it by users.

We will be using the Reddit API[^1], firstly you will need to subscribe to it which can be done via Rapid API[^2]. What about the costs though? Don't worry! It's FREE!!!

Tips: Change the **payload** as per different parameters!

## Compose message

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/composeMessage"

payload = "accessToken=%3CREQUIRED%3E&subject=%3CREQUIRED%3E&to=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&text=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Delete message

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/deleteMessage"

payload = "accessToken=%3CREQUIRED%3E&id=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Collapse Message

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/collapseMessage"

payload = "accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&id=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Send Inbox Replies

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/sendInboxReplies"

payload = "appClientId=%3CREQUIRED%3E&id=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Add a friend

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/addFriend"

payload = "name=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Friend list

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/getMyFriends"

payload = "appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Remove friend

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/removeFriend"

payload = "id=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Create Posts

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/createPost"

payload = "accessToken=%3CREQUIRED%3E&url=%3CREQUIRED%3E&title=%3CREQUIRED%3E&sr=%3CREQUIRED%3E&text=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Create a comment on posts

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/createComment"

payload = "thingId=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&text=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Edit text

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/editText"

payload = "text=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&thingId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Hide Post

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/hidePost"

payload = "appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&id=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Give Gold

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/giveGold"

payload = "accessToken=%3CREQUIRED%3E&months=%3CREQUIRED%3E&username=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Upvote

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/upVote"

payload = "id=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&rank=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Downvote

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/downVote"

payload = "rank=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&id=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Subscribe

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/subscribe"

payload = "accessToken=%3CREQUIRED%3E&subreddit=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Unsubscribe

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/unsubscribe"

payload = "accessToken=%3CREQUIRED%3E&subreddit=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Create Live Thread

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/createLiveThread"

payload = "accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&title=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Lock Thread

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/lockThread"

payload = "appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&id=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Unlock Thread

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/unlockThread"

payload = "appClientId=%3CREQUIRED%3E&id=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Get Thread Updates

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/getThreadUpdates"

payload = "appClientId=%3CREQUIRED%3E&thread=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Thread Submissions

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/getThreadSubmissions"

payload = "appClientId=%3CREQUIRED%3E&thread=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Report Thread

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/reportThread"

payload = "type=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&thread=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Search

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/search"

payload = "accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&q=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Search subreddits

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/searchSubreddits"

payload = "accessToken=%3CREQUIRED%3E&q=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Default subreddits

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/getDefaultSubreddits"

payload = "appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Search subreddits by name

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/searchSubredditsByName"

payload = "appClientId=%3CREQUIRED%3E&query=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Search Subreddits by topic

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/searchSubredditsByTopic"

payload = "accessToken=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&query=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Gold only subreddits

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/getGoldOnlySubreddits"

payload = "appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Delete subreddit image

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/deleteSubredditImage"

payload = "subreddit=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E&imageName=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Remove subreddit icon

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/deleteSubredditIcon"

payload = "subreddit=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Remove subreddit header image

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/deleteSubredditHeaderImage"

payload = "subreddit=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E&accessToken=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

## Remove multiple subreddit

```python
import requests

url = "https://redditdimashirokovv1.p.rapidapi.com/multiRemoveSubreddit"

payload = "accessToken=%3CREQUIRED%3E&multiredditOwner=%3CREQUIRED%3E&multireddit=%3CREQUIRED%3E&subredditName=%3CREQUIRED%3E&appClientId=%3CREQUIRED%3E"
headers = {
    'content-type': "application/x-www-form-urlencoded",
    'x-rapidapi-key': "fd544906eemsh58b064f09dbc569p1183abjsn8777ff646fd4",
    'x-rapidapi-host': "RedditdimashirokovV1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

***References:***

- [^1]: Reddit API, <https://rapidapi.com/dimashirokov/api/Reddit/>
- [^2]: Rapid API, <https://rapidapi.com/>
- [^3]: Subreddit, <https://www.dictionary.com/e/slang/subreddit/>
