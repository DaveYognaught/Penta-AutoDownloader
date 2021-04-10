Requirements

    python (3.8 or higher)
    streamlink (1.4.1 or higher)
    ffmpeg (Should come with Streamlink)

Setting up

    If your version of streamlink is older than 1.4.1:
        install new one and check the result with: streamlink --version-check

    Install requests module if you don't have it
        Linux: python3.8 -m pip install requests


The script will be logging to a console and to a file twitch-recorder.log

On Linux:
Run the script

	python3.8 twitch-recorder.py

To record a specific streamer use -u or --username

	python3.8 twitch-recorder.py --username forsen

To specify quality use -q or --quality

	python3.8 twitch-recorder.py --quality 720p

To disable ffmpeg processing (fixing errors in recorded file) use --disable-ffmpeg

	python3.8 twitch-recorder.py --disable-ffmpeg

If you want to run the script as a job in the background and be able to close the terminal:

	nohup python3.8 twitch-recorder.py >/dev/null 2>&1 &

In order to kill the job, you first list them all:

	jobs

The output should show something like this:

	[1]+  Running                 nohup python3.8 twitch-recorder > /dev/null 2>&1 &

And now you can just kill the job:

	kill %1