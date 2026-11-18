# Encore

A Spotify-inspired dark theme for Discord. Near-black surfaces, that signature green, pill-shaped controls, a playlist-style gradient header, a slowly drifting ambient glow and soft, floaty animations everywhere.

Works with **Vencord**, **Vesktop**, **Equicord** and **BetterDiscord**.

## Features

**Look**

- Near-black backgrounds (`#000` frame, `#121212` chat, `#181818`–`#282828` cards) with white and grey text
- Green accent on links, mentions, reactions, the selected-server pill and online dots
- A green wash that fades down from the top of the chat, like a playlist header, behind a see-through channel header
- Fully rounded buttons; green buttons use black text and grow slightly on hover
- A raised, pill-shaped message box, like a search bar
- Floating "now playing" style user panel in the bottom left
- [Figtree](https://fonts.google.com/specimen/Figtree) for text and [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) for code

**Motion**

- **Idle:** a green glow drifts behind the app, the header wash gently breathes, and the user panel and selected server bob very slightly
- **Entrances:** messages, embeds, popouts and modals drift up out of a soft blur; menus float up with their items cascading in; channels and members slide in one after another
- **Hover:** embeds and images lift like album art; server icons, reactions, avatars and toolbar icons rise; the message box lifts and glows green while you type
- **Typing indicator:** the three dots become a little green equalizer

All motion turns off when **Reduce motion** is on, either in Discord (*Settings → Accessibility*) or in your operating system.

## Installation

### Vencord / Vesktop / Equicord

1. Download [`Encore.theme.css`](Encore.theme.css).
2. In Discord, open **Settings → Vencord → Themes** and click **Open Themes Folder**.
3. Put the file in that folder.
4. Back in **Themes**, switch on **Encore**. Press `Ctrl+R` to reload Discord if it doesn't appear.

To have it update automatically instead, go to **Themes → Online Themes** and add:

```
https://raw.githubusercontent.com/MercenaryUSA/Encore/main/Encore.theme.css
```

### BetterDiscord

1. Download [`Encore.theme.css`](Encore.theme.css).
2. Open **Settings → BetterDiscord → Themes** and click **Open Themes Folder**.
3. Put the file in that folder and switch on **Encore**.

> Turn off any other theme while using Encore, or the two will clash.

## Customising

Everything is driven by the settings in section 1 at the top of the file (`:root { ... }`). Copy any of these into your **QuickCSS** to override them without editing the theme:

| Setting | Default | What it does |
|---|---|---|
| `--sp-green` | `#1ed760` | Main accent colour |
| `--sp-green-strong` | `#1db954` | Deeper accent for backgrounds and the header wash |
| `--sp-green-bright` | `#3be477` | Button hover colour |
| `--sp-teal` | `#1ab3a6` | Secondary colour in gradients and the ambient glow |
| `--sp-on-green` | `#000000` | Text colour on green buttons |
| `--sp-bg-0` / `--sp-bg-1` / `--sp-bg-2` | `#000` / `#121212` / `#0f0f0f` | App frame, chat, and channel sidebar backgrounds |
| `--sp-header-wash` | 22% green | Colour of the gradient at the top of the chat |
| `--sp-header-height` | `260px` | How far down that gradient fades |
| `--sp-ambient-speed` | `60s` | Speed of the drifting background glow (`0s` stops it) |
| `--sp-bob-speed` | `6s` | Speed of the idle floating (`0s` stops it) |
| `--sp-fast` / `--sp-med` / `--sp-slow` | `160ms` / `280ms` / `460ms` | Animation durations |
| `--sp-font` | Figtree | Interface font |

For example, to switch the accent to pink and stop the idle motion:

```css
:root {
    --sp-green: #ff4fa3;
    --sp-green-strong: #e33b8c;
    --sp-green-bright: #ff74b8;
    --sp-ambient-speed: 0s;
    --sp-bob-speed: 0s;
}
```

## Compatibility

Encore applies to Discord's **Dark**, **Darker** and **Midnight** appearance settings. Nitro profile themes keep their own colours.

Discord's class names include a hash (for example `message_SY_P2T`) that can change when Discord ships an update. If part of the theme stops applying after an update, the class names probably need refreshing; please open an issue.

## Credits

Not affiliated with or endorsed by Spotify or Discord. Fonts are served from Google Fonts, with jsDelivr as a fallback.
