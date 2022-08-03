# Hugging Face Jukebox Renderer and Job Generator 🤗

## Installation

Requires [Node.js version 16+](https://nodejs.org)

[PnPM is recommended](https://pnpm.io) but npm will work

```bash
pnpm i
sudo pnpm exec nexrender-cli
```
or
```bash
npm i
sudo npx nexrender-cli
```

## Generating job files

Open `form.html` and enter your custom inputs. The pre-filled directories and filenames only need to be changed if the project's directory structure or template files change. You'll likely only need to edit the audio filename.

`"Export JSON job file"` in the form will let you save the job file, its filename defaulting to `"<user>.json"`. A `/jobs` folder has been premade but you can save it in any location. Exporting will also save your inputs in the browser so you don't need to re-enter the working directory each time and to also allow quick iterations.

## Rendering After Effects video

Copy the generated jukebox audio file into the `/ae-template` directory and either rename it to `"output.wav"`, or set the "Audio filename" field in the form accordingly.

Then run:

```bash
pnpm render jobs/<user>.json
```
or
```bash
npm run render jobs/<user>.json
```

Rendered videos will be in the `/ae-renders` folder by default, named `"<user>.mov"`
