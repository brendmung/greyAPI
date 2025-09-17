# GreyAPI?

Welcome to **GreyAPI** — a free, lightweight API for plugging AI models into whatever you’re building. Written at odd hours, polished enough for daylight use.

## What's This All About?

GreyAPI gives you a simple way to chat with models like GPT-5, GPT-4o and more. No massive SDKs, no endless docs — just a clean API you can hit right away.

## Check It Out

You can find the actual API and demo site at: [https://grey-api.vercel.app](https://grey-api.vercel.app)

## Features
- 🧠 Access multiple AI models from one endpoint
- 💬 Just send a message, get a reply — that’s it
- 🔌 Works with JS, Python, cURL and probably your favorite language too
- 🚀 Fast enough that if it’s slow, blame your WiFi

## Basic Usage

Here's how simple it is to use (no PhD required):

### JavaScript

```javascript
async function callAPI() {
  const response = await fetch('https://grey-api.vercel.app/api/chat', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({
      model: 'gpt-5',
      messages: [
        { role: 'user', content: 'Tell me a joke about programming' }
      ]
    }),
  });
  
  const data = await response.json();
  console.log(data.response);
}
```

### Python

```python
import requests

def call_api():
    url = 'https://grey-api.vercel.app/api/chat'
    payload = {
        'model': 'gpt-5',
        'messages': [
            {'role': 'user', 'content': 'Tell me a joke about programming'}
        ]
    }
    
    response = requests.post(url, json=payload)
    data = response.json()
    print(data['response'])

# No authentication tokens, complicated SDKs...See!?
call_api()
```

## FAQ

**Q: Is this free to use?**  
A: For now, yeah! I'm keeping it open while I work on it. Might have to add some limits if it gets too popular.

**Q: Can I contribute?**  
A: Not open-source right now, but suggestions are welcome. Bonus points if they don’t make me rewrite everything from scratch.

**Q: What models are available?**  
**A:** Currently supporting GPT-5, GPT-4o, Nova AI... More might come later (if I ever figure out how to add them without breaking everything), but honestly… too lazy to keep this updated. Just go check the docs like everyone else!!

**Q: Will this make me rich and famous?**  
A: Probably not, but at least you’ll have a functioning API to brag about.


I'll post updates here when I add new features or models, so star the repo if you want to stay in the loop! No spam, I promise. I'm too lazy for that.

---

Made with ☕, vibe code and questionable life choices
