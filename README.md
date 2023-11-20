# `gen-subs`

This project uses on-device machine learning models to generate subtitles for your videos.

## Features

- 🔒 **Secure and offline** - All machine learning models are downloaded and run locally on your device. No data is sent to any server. There is zero dependency on OpenAI or other cloud services.
- 🌐 **Multilingual** - Supports a wide variety of languages. Namely,
  | Languages | | |
  | --------- | --------- | --------- |
  | 🇺🇸 English | 🇮🇳 Indian English | 🇨🇳 Chinese |
  | 🇷🇺 Russian | 🇫🇷 French | 🇩🇪 German |
  | 🇪🇸 Spanish | 🇵🇹 Portuguese/Brazilian | 🇬🇷 Greek |
  | 🇹🇷 Turkish | 🇻🇳 Vietnamese | 🇮🇹 Italian |
  | 🇳🇱 Dutch | 🇪🇸 Catalan | 🇸🇦 Arabic |
  | 🇮🇷 Farsi | 🇵🇭 Filipino | 🇺🇦 Ukrainian |
  | 🇰🇿 Kazakh | 🇸🇪 Swedish | 🇯🇵 Japanese |
  | 🇪🇸 Esperanto | 🇮🇳 Hindi | 🇨🇿 Czech |
  | 🇵🇱 Polish | 🇺🇿 Uzbek | 🇰🇷 Korean |
  | 🇫🇷 Breton | | |
- 🎨 **Customizable** - Choose from getting just an `srt` file, having the subtitles burned in to your video, and even embedding the subtitles in your video's metadata. You can also have **focus words** where the active word is highlighted in a different color.
- 🎧 **Multi-modal** - Supports both audio and video files and generates subtitles for each.
- 📊 **Multi-model** - Choose from a variety of machine learning models ranging from 40MB to >2GB in size. The larger the model, the more accurate the subtitles, but smaller models are also quite capable.

## Usage

You can generate subtitles for any video using the following command:

```bash
npx gen-subs for ./your/video.mp4
```

If you run this for the first time, you will be required to download a machine learning model to generate your subtitles. This needs to be done at least one time. Then, the program will generate a `.srt` file in your current working directory containing the subtitles for your video.

## Options

This project has a few options that you can use to customize your subtitles. Let's enumerate them here:

| Command          | Description                                         |
| ---------------- | --------------------------------------------------- |
| \`for\`          | Generate subtitles for a given video or audio file. |
| \`models\`       | Manage models                                       |
| \`models purge\` | Delete all downloaded models.                       |
| \`models ls\`    | Show a list of all models downloaded to the system. |

### \`gen-subs for [media]\`

| Option                      | Description                                                                                                      | Default                                    |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| \`-m, --model [modelName]\` | The name of the machine learning model you'd like to use to generate subtitles.                                  | \`vosk-model-small-en-us-0.15\`            |
| \`-b, --burn-in\`           | Whether to layer subtitles atop the video (burn them in).                                                        | None                                       |
| \`-e, --embed\`             | Whether to embed subtitles in the video's metadata.                                                              | None                                       |
| \`-o, --out-dir [path]\`    | Where to output the subtitle and final video files.                                                              | \`/Users/tejas/Sites/commander-to-readme\` |
| \`-f, --format [format]\`   | Choose between \`srt\` or \`ass\` formats. `ass` lets you do more cool stuff like focus words. (Default \`srt\`) | \`srt\`                                    |
| \`-h --highlight [color]\`  | (\`ass\` subtitles only) Highlight the active word with a color.                                                 | `#048BA8`                                  |

## Contributing

Please feel free to open issues and pull requests as needed and I'll try to get to them as soon as possible.

## Sustainability

This is all free and open source software. If it has helped you, please consider [sponsoring me project on GitHub](https://github.com/sponsors/TejasQ) so I can make more stuff like this and teach about it full-time.
