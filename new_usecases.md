- they only have text classifier, and have not combined their image captioning with text classifier. So can make an API to classify image using these 2 things.
- there is a existing feature request for querying image https://github.com/jerryjliu/llama_index/issues/1069
- CURRENT IDEA - organizing the new files based on where existing files are in folder. One of the tags in "extra_fields" in nodes will specify the folder name. We can exhance this further by sugeesting top k tags if the files have tag. For it's poc, we are extracting tags from research papers. Check https://github.com/jerryjliu/llama_index/issues/832 for something similar
- Check out these classes
  - https://github.com/jerryjliu/llama_index/blob/6a004797aafe80db78a8dcb5b3c085fd9586a015/llama_index/readers/file/image_caption_reader.py#L8
  - https://github.com/jerryjliu/llama_index/blob/6a004797aafe80db78a8dcb5b3c085fd9586a015/llama_index/readers/file/image_vision_llm_reader.py#L8
  - https://github.com/jerryjliu/llama_index/blob/6a004797aafe80db78a8dcb5b3c085fd9586a015/llama_index/readers/file/slides_reader.py#L56
  - https://github.com/jerryjliu/llama_index/blob/6a004797aafe80db78a8dcb5b3c085fd9586a015/llama_index/indices/query/query_transform/base.py#L174
- Audio
  - They are already making a Document object from text in Audio using openAI whisper.
  - They are already doing text to speech from VideoAudioReader class
  - No audio classification is done I think, but because the text is already in Document object, it's trivial
 
 - look into https://github.com/jerryjliu/llama_index/blob/6a004797aafe80db78a8dcb5b3c085fd9586a015/docs/gallery/app_showcase.md?plain=1#L96