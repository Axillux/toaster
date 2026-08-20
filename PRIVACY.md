# Privacy Policy

Last updated: August 2026

## Overview

Toaster ("the Bot") is an automated anti-scam moderation bot for Discord. It processes message content solely to detect scam (such as MrBeast-style giveaway scam images and texts). This policy explains what is processed, where it goes, how long it is kept, and how to have it removed.

## What the Bot processes

- **Message content:** text and images (attachments, embeds, linked images) in servers where the Bot is active. Images are fetched with strict limits (size, time, public addresses only) and validated before processing.
- **Message metadata:** message IDs, channel IDs, timestamps.
- **Author metadata:** Discord user ID and username of senders whose messages are checked, punished, or found by history scans.
- **Server configuration:** punishment choice, mute duration, log channel, custom DM template.
- **Aggregate counters:** detections, deletions, punishments per server.

## Why it is processed

To detect scam (protecting the servers the Bot serves), to execute the moderation actions configured by server administrators, and to maintain the detection database.

## Third-party processing

- **Discord API** — receiving messages, deleting them, applying punishments, sending DMs and log entries.
- **Embedding API (NVIDIA NIM)** — image and text data is transmitted to generate the vector embeddings used for scam matching (model: `llama-nemotron-embed-vl-1b-v2`). It is processed for that purpose only; no model training or fine-tuning is performed on user data.

The Bot does not sell data and shares it with no other third parties.

## Storage and retention

- Message content is processed in memory for matching and is **not** stored.
- Detected scam images awaiting an administrator's decision are stored for a limited period (default: 7 days) and purged automatically if unused.
- Approved scam/meme reference images stay in the detection database until an administrator removes them.
- Configuration and aggregate counters live in the Bot's own database, retained while the Bot serves the server.
- Technical logs may contain message IDs, user IDs and match scores for debugging, rotated by the operator's log policy.

## Direct messages

Punished users receive one DM explaining the action. Delivery depends on the recipient's own privacy settings, and the recipient can always block it.

## Your rights

- **Removal:** server administrators can remove the Bot (stopping further processing); the operator can delete stored review images and database entries on request.
- **Access:** administrators may request the metadata the Bot holds about their server.
- **Complaints:** contact the operator through the support channel listed below.

## Children

The Bot operates only inside Discord, whose Terms set a minimum age. No deliberate processing of children's data takes place.

## Changes

This policy may be updated as features change. Material changes will be announced in the support server.

## Contact

Support: https://discord.gg/wCZsphvWVr
