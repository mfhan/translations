## A sentiment-Al Journey: Sentiment Analysis Models and Literary Translation

[Svelte visuaization:] https://svelte.dev/repl/161b41989f334a12a4c2d8383831df0d?version=4.1.2

### What I wanted to find out:

I've long wondered about the quality of translations, especially when it comes to fiction. Raised in a multilingual household and having dabbled in comparative litterature at university, I always yearned to find an effective way of measuring the emotional impact of a text. After three whole hours of lecture on language models -- clearly plenty of time to understand everything about sentiment analysis -- I decided to experiment a bit.

### Summary of the data collection process, with links

-- Excerpts from _Les Miserables_, _In Search of Lost Time_ and _Wuthering Heights_ and their translations obtained from Project Gutenberg.

### Overview of the data analysis process

-- Text preparation with Python and pandas
-- Manual fine-tuning of sentence segments to ensure similarity between the two versions.
-- Sentiment analysis performed with the [twitter-XLM-roBERTa-base]("https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment") multilingual model, trained on 198 million tweets.
-- Data visualization performed with Datawrapper, then Flourish
-- Secondary data visualization experiment [conducted with D3/Svelte]("https://svelte.dev/repl/161b41989f334a12a4c2d8383831df0d?version=4.1.2").

### New skills & learning opportunities:

-- Everything took a lot more time than planned. Selecting the texts took several tried as I wanted to work on texts featuring three-dimensional characters and depicting complex emotions.
-- Sending everything into the roBERTa model also took a while. I had to re-cut text segments on several occasions.
-- Once I collected the outcomes of the sentiment anqalyses, I looked for appropriate visualization options.
-- Despite my reluctance at working with Flourish after prior misadventures, I decided to give it another try and was pleasantly surprised by the flexibility of the platform.

### What I really found:

-- I was surprised by some inexplicable labeling on non-ambiguous segments. Why does the segment "with a desperate effort" rate positive with a 0.60 score? Why is the phrase "the forgotten strains of happiness" labeled negative in English and positive in French?
-- I was surprised at the relative naivete of the model, which gave a positive label to the English sentence: "This grand little soul had taken its flight," a clear reference to death. The French sentence was correcly labeled negative with a 0.69 score.
-- My initial hunch -- that translations, by nature may tend to pick a safe middle ground and therefore be labeled as more neutral than the original, was not completely supported.
-- Another possible avenue, that some language are more polarizing than others, feels very promising.

### What I tried to do but did not have the skills/time (but might do if I had more time)

-- As always, I wish I had had more time to broaden my area of inquiry. I would like to compare translations in other language pairs, I would also, of course, experiment with other language models -- although I remain surprised at how difficult it's been to find reliable multilingual

#### Main notebook, included in this repo: lesmiz.ipynb, proust.ipynb, wuthering2.ipynb

#### Link to published page: https://mfhan.github.io/translations/
