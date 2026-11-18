Unofficial checklist: build a link that opens a Bot with a message already typed and not sent.

1. Find [BOT_ID]. Open the Bot's name, choose Share, then Copy link. The id is the last part of that link. Do not guess it from the display name.
2. Write [MESSAGE]. Ask for preparation only, and say where to stop: before sending, publishing, purchasing, paying, deleting or changing production.
3. Read the message for secrets and private details. A link is easy to forward and is kept in histories. Passwords, card numbers and keys never go into one.
4. Count the characters before encoding. The limit is 1,000.
5. URL-encode the message as a single value. A space becomes %20. Line breaks, &, #, ? and = must be encoded too.
6. Put it together: grokbot://app/v1/prompt?id=[BOT_ID]&text=<the encoded message>
7. Leave out id= only if you want the link to open the primary Bot. With no primary Bot set, such a link does nothing.
8. Decode the text value again and compare it with what you wrote. Look for cut-off text and for an extra parameter created by an unencoded &.
9. Before trying it, look at the Bot's message box. The text is added only when the box is empty, so do not lose a draft that is already there.
10. Open the link on a device where the app is installed and you are signed in. Check that the right Bot opened and the whole message is in the box.
11. The message is not sent until a person sends it. Leave it unsent while you check, and share the link only with people who should have it.
