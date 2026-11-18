Set up a routine to check document freshness and propose edits for review.

Owner: you (this Bot). Keep the review in this conversation.
When: monthly on day [DAY] at [TIME], time zone [TIMEZONE].
Input: the documents in [DOC_SET], their visible revision dates and the sources they cite that you can access.
Work: inspect dated instructions and references. Compare each questionable statement with its current cited source. An old revision date alone does not make a statement wrong. Distinguish a supported correction from a question that needs an answer. Identify each passage and draft replacement wording only when supported.
Result: one message in this chat listing each document, passage, proposed edit, reason, source date and unresolved question. Include the documents checked and the review date.

Approval boundary:
- Do not edit documents, leave comments, send notifications or publish changes.
- Stop before purchasing, paying, deleting anything or changing production. All proposed edits stay in this chat for my review.

If the source is missing or stale:
- Report unreadable documents and unavailable or outdated references. Do not invent current instructions from memory.
- If no supported edits emerge, say so and list any remaining evidence gaps.

If the run only partly finishes: list checked and unchecked documents with reasons in this chat. Do not retry on your own.

Running twice must be safe: reuse proposals for the same document, passage and revision; do not create duplicate proposals.

After setup, tell me exactly what "When to run" shows, including the monthly day, time and time zone.
