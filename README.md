# Scrawl

A multiplayer draw-and-guess game for friends. It runs entirely in the browser: no server and no accounts.

**Play:** https://harshgaba1196.github.io/scrawl/

## How it works

1. Open the page, pick a name and click **Create a room**. You're the host, so keep that tab open.
2. In the lobby, click **Copy invite link** and send it to your friends.
3. They open the link, type a name and press **Join**.

Game messages travel over free public MQTT brokers (EMQX, with HiveMQ as a fallback) on secure WebSockets, so rooms work on any network that can load websites. Every message is encrypted in the browser with a key derived from the room code, so the broker only sees scrambled data.

## Features

- Easy, medium and hard words, worth 1×, 1.3× and 1.6× points
- Pen, eraser, fill bucket, line, rectangle, ellipse, undo and redo
- Letter hints over time, close-guess alerts, streak bonuses
- Live emoji reactions and a "Love this drawing" button
- Nine word packs plus secret custom words
- Podium and a gallery of every drawing at the end
