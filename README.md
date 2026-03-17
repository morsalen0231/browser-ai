<div align="center">

# Morai LLM Chat

<a href="https://github.com/morsalen0231/browser-ai"><img alt="Repository" src="https://img.shields.io/badge/Repo-morsalen0231%2Fbrowser--ai-222?logo=github&logoColor=white"></a>
<a href="https://morsalen.netlify.app"><img alt="Live Site" src="https://img.shields.io/badge/Live-morsalen.netlify.app-32a852?logo=netlify"></a>
<a href="https://discord.gg/9Xpy2HGBuD"><img alt="Join Discord" src="https://img.shields.io/badge/Join-Discord-7289DA?logo=discord&logoColor=white"></a>

**Private AI Conversations, Fully In-Browser.**

[**Chat Now**](https://morsalen.netlify.app/)

[Morai LLM Demo Video](https://github.com/morsalen0231/browser-ai/assets/demo)

</div>

## Overview

**Morai LLM Chat** is a private AI chat interface that runs natively in your browser with WebGPU acceleration. Enjoy an unprecedented, private, and accessible AI conversation experience.

## Key Features

- **Browser-Native AI**: Experience cutting-edge language models running natively within your web browser with WebGPU acceleration, eliminating the need for server-side processing or cloud dependencies.
- **Ganranteed Privacy**: With the AI model running locally on your hardware and all data processing happening within your browser, your data and conversations never leave your computer, ensuring your privacy.
- **Offline Accessibility**: Run entirely offline after the initial setup and download, allowing you to engage with AI-powered conversations without an active internet connection.
- **Vision Model Support**: Chat with AI by uploading and sending images, making it easy to get insights and answers based on visual content.
- **User-Friendly Interface**: Enjoy the intuitive and feature-rich user interface, complete with markdown support, dark mode, and a responsive design optimized for various screen sizes.
- **Custom Models**: Connect to any custom language model on you local environment through [MLC-LLM](https://llm.mlc.ai/). For detail, check the [Use Custom Models](#use-custom-models) section.
- **Open Source and Customizable**: Build and customize your own AI-powered applications with our open-source framework.

## Built-in Models

Morai LLM ships with a curated set of in-browser models that run with WebGPU.

## Use Custom Models

You can point Morai LLM to any compatible REST endpoint to load your own model.

## Development

```shell
# 1. install nodejs and yarn first
# 2. config local env vars in `.env.local`
# 3. run
yarn install
yarn dev
```

## Deployment

### Build

You can build the application as a Next.js build using `yarn build` or as a static site using `yarn export`. For more information, check [Next.js documentation](https://nextjs.org/docs/pages/building-your-application/deploying);

### Docker

```shell
docker build -t webllm_chat .
docker run -d -p 3000:3000 webllm_chat
```

You can start service behind a proxy:

```shell
docker build -t webllm_chat .
docker run -d -p 3000:3000 \
   -e PROXY_URL=http://localhost:7890 \
   webllm_chat
```

If your proxy needs password, use:

```shell
-e PROXY_URL="http://127.0.0.1:7890 user pass"
```

## Community and Contributions

Morai LLM thrives on community involvement. Join us on Discord to connect with fellow developers.
