# Screen recording on Mobian
It's easiest to start and stop the recording over SSH.

- `sudo apt install wf-recorder`
- To start: `wf-recorder -f FILENAME.mp4`.
- To stop, use Ctrl C.

# Screenshots on Mobian
- `sudo apt install grim`
- To take a screenshot: `grim FILENAME.png`.
- Either use the command over SSH, or use `sleep N; grim` to wait N seconds before taking the screenshot.