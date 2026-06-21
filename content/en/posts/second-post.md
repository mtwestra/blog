+++
date = '2026-06-10T09:00:00+02:00'
draft = false
title = 'The context window is not memory'
tags = ['llm', 'architecture']
+++

One of the most common misconceptions I see in teams starting to build with LLMs is treating the context window as memory. It isn't. It's more like a whiteboard — extremely useful while it's in front of you, but the moment you walk out of the room, it's gone.

The context window is finite, expensive, and ephemeral. Every token you put in it costs money on the way in and slows down generation on the way out. And when the conversation ends, everything in it disappears. The model has not learned anything from your exchange. Tomorrow it will not remember you.

This matters enormously for product design. If you want an AI assistant that knows your history, you need to build that memory layer yourself — typically some combination of a vector database for semantic retrieval and structured storage for facts that need to be exact. The LLM is then a reasoning engine that operates on whatever you retrieve and inject into the prompt.

The teams that build the best AI products understand this architecture clearly. They think about what needs to persist, how to retrieve it efficiently, and what can safely be reconstructed from scratch each time. The context window is a powerful tool. It's just not a filing cabinet.
