# yt2text

Python library for extracting text from a YouTube video in a single command, using OpenAi's Whisper speech recognition model. It doesn't use disk, performs everything in memory.

https://pypi.org/project/yt2text/

### Installation:
```
pip install yt2text
```
Whisper requires **ffmpeg** to be installed in your computer. Check Whisper's requirements
https://github.com/openai/whisper#setup

### Usage:

You'll only interact with the get_text function. It takes a YouTube URL as an argument and returns the text as a string.

```python
import yt2text

text = yt2text.get_text("https://www.youtube.com/watch?v=fLeJJPxua3E")
print(text)
```

### Optional Arguments:
**model**: 
Set Whisper model (tiny,base,small,medium or large). Check here for details:
https://github.com/openai/whisper#available-models-and-languages

Defaults to "base" which should be good enough for most cases.
The first time you use a model, it will be downloaded first.

**verbose**
Set True to print each step of the process. Defaults to False, it only prints if there is an error.

### Usage with optional arguments
```python
import yt2text

text = yt2text.get_text("https://www.youtube.com/watch?v=fLeJJPxua3E", model="medium", verbose=True)
print(text)
```

## Contact
Raise an Issue in this Github repo (preferred, it sends a notification to my phone)
Or mail me at atahanuz23@gmail.com







