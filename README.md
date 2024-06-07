# NER-Location-extraction-and-geocoding
This script automates the extraction and visualization of location information from unstructured text, particularly focusing on security incidents in conflict zones. It utilizes a local Large Language Model (LLM) to ensure privacy while extracting location details from sensitive text, which are then formatted for submission to a geocoding system. Google Maps is employed in this implementation, but users can configure and use an in-house OpenStreetMap geocoding system or any other for enhanced privacy and autonomy. The resulting locations are plotted on an interactive map using Folium, facilitating comprehensive visual analysis. This workflow enables users to process sensitive data locally, addressing privacy concerns and providing detailed geographical insights for informed decision-making.

Additionally, the script leverages LMStudio (https://lmstudio.ai/) in local server mode, ensuring privacy, easy testing, and seamless switching between multiple models. Performance testing on a local machine with an Nvidia T1200 4GB GPU indicates good performance. Performance for the extraction can be improve by using a more powerful LLM localy or an online one like ChatGPT.
  

## Features:

Extracts and structures location data from Excel files containing conflict-related security incidents.
Utilizes a local Large Language Model (LLM) for privacy-preserving location extraction.
Formats extracted data for submission to Google Maps' geocoding system.
Visualizes finalized locations on an interactive map using Folium.
Exported to a .csv file for further analysis.

## Usage:

Ensure LMStudio (https://lmstudio.ai/) is set up and runs a local server mode.
The following models were tested for location extraction:
- Phi-3-mini-128k-instruct-GGUF-Imatrix-smashed (https://huggingface.co/PrunaAI/Phi-3-mini-128k-instruct-GGUF-Imatrix-smashed)
- OpenHermes-2.5-Mistral-7B-GGUF (https://huggingface.co/TheBloke/OpenHermes-2.5-Mistral-7B-GGUF)
Larger models can be used and will improve results, but will require a more powerful GPU.

You will need a Google Map API key to run the code. If not, you can set up your own instance of OSM or use Nominatim

## Specifications:
Tested on a local machine with an Nvidia T1200 4GB GPU, the script demonstrates good performance with the specified models.
