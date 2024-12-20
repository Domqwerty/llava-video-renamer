# LLaVA Video Renamer: Automatically Rename Videos with LLaVA

This repository contains a Google Colab notebook that utilizes the LLaVA model (version **llava-v1.5-7b**) to automatically rename video files based on their content. The script extracts the first frame from each video, generates a detailed description in **Italian** using LLaVA, and renames the video file using a truncated and hashed version of the description.

## Features

- **Automatically renames** video files based on content.
- **Extracts the first frame** from each video.
- **Generates Italian descriptions** using the LLaVA model (llava-v1.5-7b).
- **Truncates and hashes** the description to create unique and limited-length filenames.
- **Supports batch processing** of multiple videos in a folder.
- **Easy to use** in Google Colab.

## How to Use the Notebook

1. **Open the notebook in Google Colab:**
   - Click on the following link: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Domqwerty/llava-video-renamer/blob/main/llava_video.ipynb)
   - Or, download the notebook (`.ipynb`) from this repository and upload it to Google Colab.

2. **Install the dependencies:**
   - Run the first cell of the notebook to install the required libraries (transformers, OpenCV, etc.).

3. **Download the LLaVA model:**
   - Ensure you have downloaded the `llava-v1.5-7b` model (or modify the `model_path` variable in the notebook if you are using a different model).
   - Instructions for downloading the model are included in cell 3 of the notebook.

4. **Upload your videos:**
   - Create a folder named `videos` in the "Files" tab of Colab (left sidebar).
   - Upload all the videos you want to rename into the `videos` folder.

5. **Run the notebook:**
   - Run all cells of the notebook in order.
   - The script will extract the first frame from each video, generate an Italian description, and rename the file.

6. **Download the renamed videos:**
   - Once the process is complete, compress the `videos` folder into a `.zip` archive (instructions in the final cell of the notebook).
   - Download the `.zip` archive containing the renamed videos.

## Requirements

- Google Colab
- LLaVA model (llava-v1.5-7b or compatible)
- Python 3.x
- `transformers`
- `opencv-python`
- `gradio`
- Other dependencies specified in the `requirements.txt` file (if present)

## Customization

- **Prompt:** You can modify the prompt used to generate descriptions in cell `6` of the notebook (or in the `process_videos_in_folder` function).
- **Filename length:** You can change the maximum filename length (truncation) and the number of hash characters in the `rename_video` function.
- **LLaVA model:** You can use a different LLaVA model by modifying the `model_path` variable.

## Notes

- Make sure you have enough storage space in Google Colab for the videos and the LLaVA model.
- Processing time depends on the number of videos, their length, and the power of the Colab GPU.
- This script has been tested with the `llava-v1.5-7b` model. Other models may require code modifications.

## License

This project is released under the MIT License. See the `LICENSE` file for more details.

## Author

[Your name and/or your GitHub username]

## Contributions

Contributions are welcome! If you want to contribute to this project, please fork the repository, make your changes, and submit a pull request.
