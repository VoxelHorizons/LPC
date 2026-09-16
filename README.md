# LPC
A chat formatting plugin for LuckPerms.

## Signed chat on Paper

LPC preserves Paper's original player message component by default and applies prefixes, names, suffixes, PlaceholderAPI output, and format colours through Paper's `ChatRenderer`.

This avoids replacing the player-authored message during normal formatting, allowing the original client-signed message to remain associated with the delivered chat.

The default configuration is:

```yaml
secure-chat:
  preserve-signatures: true
```

When signature preservation is enabled, LPC does not transform player-entered colour codes such as `&aHello` or `&#ff0000Hello`, because doing so changes the content the client originally signed. Formatting colours configured in `chat-format`, LuckPerms metadata, and surrounding placeholders continue to work normally.

Servers that explicitly prefer LPC's legacy player-message colour processing can set `secure-chat.preserve-signatures` to `false`.
