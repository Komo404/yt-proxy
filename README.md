# yt-embed

A minimal GitHub Pages proxy for embedding YouTube videos from contexts where `youtube-nocookie.com` blocks the referrer, such as browser extensions.
Created this to use in my moz extension NamaStream

## Why

Browser extensions run under a `moz-extension://` or `chrome-extension://` origin. YouTube's embed endpoint rejects these as invalid referrers (error 153). Hosting the embed on GitHub Pages gives it a valid `github.io` referrer that YouTube accepts.

## Usage

```
https://komo404.github.io/yt-embed/?v=VIDEO_ID
```

### Parameters

| Param | Description |
|--|---|
| `v` | Required 4 YouTube video ID |
| `autoplay` | Autoplay on load |
| `mute` | Muted (required for autoplay) |
| `start` | Start at a given second |

### Example

```
https://komo404.github.io/yt-embed/?v=dQw4w9WgXcQ&autoplay=1&mute=1
```

## Setup

1. Fork or clone this repo
2. Go to Settings, then Pages and set the source to the `main` branch
3. The page will be live at `https://YourAccount.github.io/yt-embed/`

## Notes

- Uses `youtube-nocookie.com` to minimize tracking cookies
- `rel=0` and `modestbranding=1` are applied by default
