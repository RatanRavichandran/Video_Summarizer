# Video_Summarizer
Implementing a Youtube video summarizer using BERT, Google APIs and OpenAI's Whisper models.

# About the Project

In today's digital realm, video storytelling is crucial. This project uses OpenAI's Whisper system to improve user experience wrt youtube videos. It transcribes and summarizes videos, giving viewers versions of long videos, peppered with relevant visuals sourced from Google searches.

# Datasets
Any youtube video can be used as a dataset for this project. I've used a video talking about The Great Depression.

# Methodology

**Methodology**

1. **User Input - YouTube Video URL:** 
   - Obtain the YouTube video URL from the user, which serves as the input for the project.
   
2. **Whisper Transcription:**
   - Use OpenAI's Whisper system to convert the audio from the provided YouTube video URL to text.
   
3. **Text Summarization with BERT:**
   - Implement the BERT (Bidirectional Encoder Representations from Transformers) model for text summarization.
   - Summarize the transcribed text to create concise summaries of the video content.
   - Analyze the quality of the summary obtained using ROUGE metrics.
   
4. **Keyword Extraction with KeyBERT:**
   - Utilize KeyBERT for keyword extraction.
   - Identify and extract key terms and phrases from the video transcript to serve as focal points.
   
5. **Image Retrieval:**
   - Implement a model using Google API calls to retrieve relevant Google search images based on the extracted keywords.
   
6. **Text Overlay:**
   - Overlay the extracted key sentences from the video transcript onto the retrieved images.
   
7. **Short-Form Video Creation:**
   - Integrate the visualized keywords and sentences to create short-form videos.
   - Ensure proper sequencing and synchronization of visual and textual elements.

## Architecture

<a href="https://ibb.co/DRvTgF6"><img src="https://i.ibb.co/kSwv6Tr/image.png" alt="image" border="0"></a>

Figure 1: Project Architecture

# Results
The model successfully extracts the audio from the youtube video. This audio is saved as `demo.mp4`.
Demo.mp4 is then transcribed, using the Whisper model. This transcription text is also saved, as `demo.txt`
This demo text file is summarized using the BERT Model, and a new summarized text file is created called `short_summary_demo`.
This text file is analyzed and keywords are identified using the KeyBERT. For each of these keywords, google images of the searches of those keywords are retrieved using the Google Images API.
It then outputs a video captioning these images, shown as `VidSummFinal`.

# Contributions
If you have ideas for improvement or wish to contribute, please open an issue or submit a pull request. Collaboration is highly encouraged!
