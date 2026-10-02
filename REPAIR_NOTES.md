# Revision 21

Legacy UI hiding is disabled to prevent blank spaces and unintended hidden containers. Restart YouTube after updating to clear existing hidden views. The player-ad hooks remain enabled.

The feed model filter is native code in YouTube-JH experimental 1.8.2-exp3 and needs that dylib installed once. Remote version 1.8.2-exp2 describes rules only. The new binary shows native and rule versions separately. Unknown renderer formats remain visible rather than hiding an entire feed.

Signatures and SHA-256 of decoded payload were verified, including rejection of modified payloads. Revision 20 is retained for history; the active manifest points to revision 21.
