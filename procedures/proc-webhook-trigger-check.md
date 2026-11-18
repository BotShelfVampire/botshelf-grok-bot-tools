Unofficial checklist: check that a webhook-triggered routine starts from a call you control, and read what the run did.

1. Find [ROUTINE_NAME] in the Details of the Bot that owns it. Check that it is the routine you mean.
2. Read its approval boundary first. A webhook call starts real work. Sending, publishing, purchasing, paying, deleting and production changes must stop for approval.
3. On desktop, open the routine's Webhook section. Note where "POST to" (the address) and the key are shown. Do not copy them into chat, notes or a repository.
4. Write [SAFE_PAYLOAD]: a small, harmless body with no secrets, no customer data and no text that reads like an instruction.
5. Keep the key in an environment variable or a secret store on the machine that makes the call. Never paste it into a saved example.
6. Prepare one POST request to the shown address with the header Authorization: Bearer <key> and the safe payload as the body.
7. Send it once. If the address, key or payload is in doubt, do not send.
8. Read the response code. 200 means the run started, not that it finished. Any other response means no run started.
9. Open the routine's run records and find this run. Wait for it to end before you judge it.
10. Compare the result with the payload you sent. Look for missing work and for actions held for approval.
11. Write down the response code, the result and what is still open. Leave the key and the address out of your notes.
12. If the key may have leaked, stop calling it. The pages we read do not describe replacing a key: ask the Bot how to replace it, or delete the routine and set it up again. Deleting a routine cannot be undone, so decide that yourself.
