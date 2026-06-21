+++
date = '2026-06-18T09:00:00+02:00'
draft = false
title = 'Prompting is a skill, not a trick'
tags = ['prompting', 'llm']
+++

There's a temptation to treat prompt engineering as a collection of magic incantations: add "think step by step", wrap everything in XML tags, tell the model it's an expert. Some of these techniques do work, in specific contexts, for specific tasks. But approaching prompting as a bag of tricks leads to brittle systems that break when the model is updated or the task shifts slightly.

The more durable mental model is that prompting is communication. You're trying to give a very capable but context-free collaborator enough information to do a specific job well. That means being clear about the goal, the constraints, the format you want, and what a good result looks like. The same skills that make you a good writer of specifications make you a good prompt engineer.

What this implies practically: invest time in understanding why a particular prompt works, not just that it does. When you get a bad output, diagnose whether the model misunderstood the task, lacked information, or was given conflicting instructions. Then fix the root cause. Layering on more instructions without understanding the failure mode just makes the prompt longer and more fragile.

The best prompts I've seen are often shorter than you'd expect. They're precise about what matters and silent about what doesn't. That clarity is hard to achieve, but it scales in a way that prompt hacks don't.
