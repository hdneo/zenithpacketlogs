Zenith capture – sanitized export
Created: 2026-11-07 21:58   HTTP entries: 44   ZenFabric messages: 82597

Included files:
  zenfabric.log               readable (hex/ASCII, MxO style)
  zenfabric-decrypted.pcap    for Wireshark
  zenfabric.jsonl / .zfcap    machine-readable (ZenithSniffer decode)
  http.log / http.jsonl       web requests (login, realms, PlayFab, Nexus)

What was sanitized:
  - sessions.jsonl (tokens, session keys) and passive raw data (IP addresses) are NOT included
  - tokens, session tickets, auth headers, e-mail, user names, Steam/Oculus/PlayFab IDs,
    character names and account fields were replaced with pseudonyms of the same length
    (the same player has the same pseudonym throughout the export; not reversible)
  - client address replaced with 10.0.0.2; server addresses (public game servers) are kept

NOT removed automatically: free text typed by players (e.g. chat messages, guild names, notes).
So don't write anything personal in chat while capturing.

Statistics:
  AuthWorker: key parts zeroed                            1
  replaced: HTTP header Cookie                            1
  replaced: HTTP header Set-Cookie                        1
  replaced: JSON: authToken                               1
  replaced: JSON: code                                    1
  replaced: JSON: email                                   1
  replaced: JSON: playFabId                               1
  replaced: JSON: sessionTicket                           1
  replaced: JSON: user_id                                 1
  replaced: JSON: username                                1
  replaced: PlayFab ID                                    91
  replaced: component 1008                                38
  replaced: sessions: identityToken                       1
  replaced: sessions: joinToken                           1
  replaced: sessions: symmetricKeyHex                     1
  replacements in ZenFabric data                          2147

Self-check: no original values found in the export.
