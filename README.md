# dat.json

The WIP specification for the dat.json meta format.

```json
{
  "title": "My paper library",
  "author": "Julian Gruber <julian@juliangruber.com>",
  "url": "dat://c75ffb161a9965e47323ba9b76aa11f649504b0d2d5d062dcb3438d5aeadc187"
}
```

## Specification

Add a `dat.json` with any of those keys - all are optional - to the root of a dat archive to help tooling work with your archive more nicely:

### `.title`

A short but descriptive human friendly title.

### `.description`

A one- or two-line description of the archive.

### `.url`

Url of the Dat archive. This will usually be the `dat://` then the archive key.

### `.author`

The archive's author - the packager, not necessarily the data's author as well. Can be either an object with any of those keys:

```json
{
  "name": "Julian Gruber",
  "email": "julian@juliangruber.com",
  "web": "https://juliangruber.com"
}
```

or a string with at least the name and any of the segments email and web:

```js
"NAME <EMAIL> (WEB)"
```

like for example:

- `"Julian Gruber"`
- `"Julian Gruber <julian@juliangruber.com>"`
- `"Julian Gruber (https://juliangruber.com/)"`
- `"Julian Gruber <julian@juliangruber.com> (https://juliangruber.com/)"`

## Support

- [Dat-Desktop](https://github.com/juliangruber/dat-desktop) will use `.title` to display a nice archive name instead of just its key
