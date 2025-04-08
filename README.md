# Grey API 🤖

"Wait, how did you even find this place? Got lost on GitHub?, or were you actually looking for this? Either way, welcome! I built this API service to give you easy access to some powerful AI models without all the boring stuff."

## What's This All About?

Grey API is my little project that gives you access to powerful AI models without all the hassle. I built a super simple API that lets you chat with models like GPT-4o and others without having to deal with complicated setups. Because let's be honest, nobody has time to read 50-page documentation just to ask an AI "Why did the chicken cross the road?" (bad joke lol)

## Check It Out

You can find the actual API and demo site at: [https://grey-api.vercel.app](https://grey-api.vercel.app)

## Features

- 🧠 Access to multiple AI models through one API
- 💬 Simple chat endpoint (so simple even your grandma could use it)
- 🔌 Easy to integrate with your projects (easier than assembling IKEA furniture)
- 🚀 Works with JavaScript, Python, cURL, Java, etc.

## Basic Usage

Here's how simple it is to use (no PhD in computer science required):

### JavaScript

```javascript
async function callAPI() {
  const response = await fetch('https://grey-api.vercel.app/api/chat', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({
      model: 'gpt-4o',
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
        'model': 'gpt-4o',
        'messages': [
            {'role': 'user', 'content': 'Tell me a joke about programming'}
        ]
    }
    
    response = requests.post(url, json=payload)
    data = response.json()
    print(data['response'])

# Look ma, no authentication tokens or complicated SDKs!
call_api()
```

## FAQ

**Q: Is this free to use?**  
A: For now, yeah! I'm keeping it open while I work on it. Might have to add some limits if it gets too popular (haha).

**Q: Can I contribute?**  
A: This isn't an open-source project right now, but feel free to suggest ideas! I'm particularly fond of ideas that don't require me to rewrite everything from scratch.

**Q: What models are available?**  
**A:** Currently supporting GPT-4o, GPT-3.5 Turbo, and Nova AI. More might come later (if I ever figure out how to add them without breaking everything), but honestly… too lazy to keep this updated. Just go check the docs like everyone else! 😎

**Q: Will this make me rich and famous?**  
A: Probably not, but neither will pretending to code while secretly browsing cat memes.


I'll post updates here when I add new features or models, so star the repo if you want to stay in the loop! No spam, I promise. I'm too lazy for that.

---

Made with ☕, vibe code, and a concerning amount of late-night debugging sessions
