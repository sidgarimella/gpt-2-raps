# gpt-2 raps

A neural rap lyrics generator powered by [GPT-2](https://blog.openai.com/better-language-models/), ported from [gpt-2-poetry](https://github.com/kylemcdonald/gpt-2-poetry) by [@kcimc](https://twitter.com/kcimc/).

## Example

Demo running [here](https://ewenme.github.io/gpt2-raps/).

## Setup

- R, [geniusr](https://github.com/ewenme/geniusr) for sourcing original lyrics from [Genius](https://genius.com/)
- Python, [GPT-2](https://github.com/openai/gpt-2/) for generating lyrics (follow [these installation instructions](https://github.com/openai/gpt-2/blob/master/DEVELOPERS.md) for GPT-2)

## Contents

Input:

- Genius song IDs stored in `genius_song_ids.txt`

src:

- `00_requirements.R` installs/loads required R libraries
- `01_get-raps.R` gets lyrics from Genius for tracks in `genius_song_ids.txt`, then exports to text files
- `02_gen-raps.ipynb` makes new lyrics based on random chunks from existing lyrics and seed words (should be run from your `gpt-2/src/` directory)

Output:

- `[0-9].txt` lyrics as text files (generated by `01_get-raps.R`)
- `lyrics.json` all original lyrics as JSON
- `generated.json` all generated lyrics as JSON

`index.html` houses the demo app.


