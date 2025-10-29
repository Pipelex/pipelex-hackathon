# Hackathon - Do the impossible with AI

We are happy to welcome you to our hackathon to celebrate our first official launch!! 🎉

- Don't hesitate to give us some feedback, and a star 🌟 on github! [--> RIGHT HERE <--](https://github.com/Pipelex/pipelex)
- You can also bump a like 🤝 on devhunt [--> RIGHT HERE <--](https://devhunt.org/)

## Resources

### Support

Since we are in early stage, you might encounter issues. Don't hesitate to reach out to us for debugging

- **Support Channel:** [join our discord](https://go.pipelex.com/discord). We have created a channel for the hackathon.
- Look for Thomas, Louis or Robin. We have Pipelex merch and a french accent, you can't miss us.

### Documentation

- **Documentation:** [https://docs.pipelex.com]
- **API Reference:** [https://docs.pipelex.com/pages/api/]

---

## ⚠️⚠️⚠️ IMPORTANT: Focus on ONE Feature! ⚠️⚠️⚠️

**You have only 2 hours and 30 minutes.**

- Pick ONE concrete problem to solve.
- Think about the data right from the beginning.
- Build ONE workflow that actually works
- Integrate it into a simple, functional app
- Make it demo-ready

**Remember:** A single feature that works beautifully is infinitely better than five half-baked ideas. Focus, ship, and shine! 🎯

## Setup

### Getting Started

### OPTION 1 (Easiest - less setup): Python Frontend

Build your frontend with **Streamlit** or **Gradio** or else.

**Step 1: Install Pipelex**

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install pipelex
```

**Step 2: Configure your environment variables**

Create a `.env` file in your project directory and add your BlackboxAI API key:
If you don't have one, come to us.
```
BLACKBOX_API_KEY=your_blackbox_api_key
```

**Step 3: Initialize Pipelex**

```bash
pipelex init
```

When it comes to choosing the backend, choose "BlackboxAI" (number 11).

![Backend Selection](backend.png)

**Step 4: Configure the routing profile**

Open the file `.pipelex/inference/routing_profiles.toml` and modify the `active` value:

```toml
active = "all_blackboxai"
```

**Step 5: Verify your setup**

```bash
pipelex doctor
```

Run this command to make sure everything is configured correctly.

**Step 6: Build your workflow**

```bash
pipelex build pipe "Create me a workflow that..."
```

Help here to execute the workflow [Pipelex documentation](https://docs.pipelex.com/pages/build-reliable-ai-workflows-with-pipelex/design_and_run_pipelines/#running-a-pipeline) to:


**Step 7: Build your frontend**

Use Streamlit or Gradio to create a UI that calls your Pipelex workflows.

✅ No API server needed - Pipelex runs directly in your Python code!

---

### OPTION 2 (Docker) - TypeScript Frontend

Build your frontend with **Next.js**, **Vue.js**, **React**, etc.

**Requirements:** Docker installed ([Install Docker](https://docs.docker.com/desktop/setup/install/mac-install/))

**Run the Pipelex API:**

```bash
docker run --name pipelex-api -p 8081:8081 \
  -e API_KEY=pipelex-hackathon-2025 \
  -e BLACKBOX_API_KEY=your-blackbox-api-key-here \
  pipelex/pipelex-api:latest
```

✅ The API will be available at `http://localhost:8081`

Here is the API documentation: [Pipelex API Documentation](https://docs.pipelex.com/pages/api/)

## How to Submit

**[Link to submission form]**

You will need to provide by 9pm:

1. **GitHub Repository Link**
   - Make sure your repository is public or accessible

2. **Demo Video Link** (YouTube, Loom, or similar)
   - **Maximum 3 minutes**
   - Show your workflow in action
   - Demo the app functionality

---

Good luck, and happy hacking! 🎉
