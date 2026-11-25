---
name: voice-generation
description: Produce a finished Arabic (Khaleeji, Egyptian or MSA) voice-over from a script, using only a phone and free tools. Claude cannot make audio itself. So Claude writes the spoken script (clean, ear-friendly, one clip per line), writes the voice direction (persona, pace, mood), and gives the exact few taps to turn it into a downloadable audio file in Google AI Studio (free, no card) with a fallback route. Use when the user wants a voice-over, narration, TTS, a Khaleeji or Egyptian voice, or audio for a reel, TikTok or Short. Pairs with the video-generation skill (audio first, then real clip durations).
---

# Voice Generation (phone-only, free)

## Honest capabilities (say these plainly to the user)

- Claude **writes** the voice-over: the lines, the pauses, the voice direction. Claude does **not** output audio or an mp3 itself, and cannot call outside TTS services from the chat.
- The audio is made in a **free web tool on the phone** (Google AI Studio, the user's own Google account). It takes about 1 minute per clip.
- Dialect: the free model reads Arabic well and follows a dialect description in text, but there is no built-in "Khaleeji" switch. The user must listen once and judge. Egyptian and MSA are the safest. Khaleeji works by writing the lines in Khaleeji spelling and describing the voice, so tell the user it may need one retry.
- Free limits and model names change. If the tool asks for billing or a card, stop and use the fallback. Never suggest paying.
- Do not put customer data, private names, numbers or confidential text in the script. Free-tier text may be used by Google to improve its products.

## Workflow

1. **Get the inputs** (ask only what is missing, one short message): the script or idea, the dialect (Khaleeji / Egyptian / MSA), male or female, the mood (energetic, calm, serious).
2. **Write the spoken script.** Follow `references/script-for-voice.md`. One idea per line, 8 to 14 words max per line, written exactly as it should be spoken, in the chosen dialect's spelling. Number the lines 1..N. Target 2.5 to 3.5 seconds per line for reels.
3. **Write the voice direction** (one short Arabic or English paragraph): who is speaking, dialect, pace, energy. Use the templates in `references/script-for-voice.md`. Keep it separate from the lines. Never mix direction into a line, because it will be read aloud.
4. **Give the user the exact steps** from `references/ai-studio-steps.md`, in their language, as a short numbered list. Give the lines as a copy-friendly list.
5. **Ask for the result.** The user listens and replies "good", or says which line to redo (too fast, wrong dialect, mispronounced word). Fix the spelling or the direction and give only the changed line again. For mispronounced words see the pronunciation table in `references/script-for-voice.md`.
6. **Hand off.** If this is for a video: ask for each clip's duration in seconds (one number per clip) and pass them to the video-generation skill so scene timing uses real lengths.

## Fallbacks (use only if AI Studio fails or hits a limit)

Read `references/fallbacks.md`. Pick ONE fallback, not a list. The most reliable one is the user recording their own voice in CapCut, using the script Claude wrote.

## Rules

- One route at a time. Do not list five sites.
- Free only. No card, no trial, no VPN.
- Arabic-first, same language as the user. Egyptian Arabic for chat with the user unless they write otherwise.
- Never claim you heard the audio. Claude cannot hear it. Only the user can judge the voice.
- Keep numbers, dates and names spelled in words if the voice reads them wrong.
