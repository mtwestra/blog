+++
date = '2026-06-01T09:00:00+02:00'
draft = false
title = 'Why AI agents are harder than they look'
tags = ['agents', 'llm']
+++

Everyone is building AI agents right now. The demos are impressive: an LLM browses the web, writes code, sends emails, books meetings. It looks like magic. But if you've tried to deploy one in a real production environment, you know the gap between demo and reliable product is enormous.

The core problem is that language models are probabilistic. They don't execute a plan deterministically — they sample from a distribution of likely next tokens. Most of the time that produces something sensible. But chain enough of those steps together, and the tail risks compound. A five-step agent that's 95% reliable at each step has only a 77% chance of completing without error. Ten steps drops that to 60%.

This isn't a reason to give up on agents. It's a reason to design them carefully: keep loops short, add checkpoints, make failures recoverable, and keep a human in the loop for anything consequential. The teams shipping reliable agents aren't the ones with the most powerful models — they're the ones who treat the agent like a junior employee on their first week, not an autonomous oracle.

The mental model shift required is significant. We're used to software that either works or throws an exception. Agents introduce a third category: plausibly wrong. Building the intuition to catch that — before it causes damage — is the real engineering challenge of this moment.
