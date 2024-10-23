# Run Audio Through FFMPEG

## Oneliner

```bash
git clone git@github.com:jadujoel/piper.git && cd piper && npm install && node index.mjs
```

Above will clone the repo, install the dependencies and start the app (as long as you have ffmpeg in your path).

## Setup

```bash
npm install
```

## Configuration

In `Piper.toml`
Set the path to ffmpeg depending on where you have it located.
In the filters array, set which audio filters you want to use.

example toml
```toml
ffmpeg_path = "node_modules/ffmpeg-helper/win32-x64.exe" # Windows
# Size of the ring buffer (higher values mean more latency but less chance of audio dropouts)
buffer_size = 10240
filters = ["arnndn=m=bd.rnnn"]
input_device_name = "BlackHole 2ch"
output_device_name = "MacBook Pro Speakers"
```

You may leave out the input_device_name and output_device name and the program will prompt you instead.

## Usage

Start the app:

```bash
node index.mjs
```

or

```bash
npx pipe-through-ffmpeg
```
