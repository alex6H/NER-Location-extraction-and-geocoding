# NER-Location-extraction-and-geocoding
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-green.svg)](https://python.org)
[![GitHub stars](https://img.shields.io/github/stars/alex6H/NER-Location-extraction-and-geocoding.svg?style=social&label=Star)](https://github.com/alex6H/NER-Location-extraction-and-geocoding)
[![GitHub forks](https://img.shields.io/github/forks/alex6H/NER-Location-extraction-and-geocoding.svg?style=social&label=Fork)](https://github.com/alex6H/NER-Location-extraction-and-geocoding/fork)
[![GitHub last commit](https://img.shields.io/github/last-commit/alex6H/NER-Location-extraction-and-geocoding.svg)](https://github.com/alex6H/NER-Location-extraction-and-geocoding/commits/main)
[![GitHub Views](https://komarev.com/ghpvc/?username=alex6H&repo=NER-Location-extraction-and-geocoding&color=brightgreen&style=flat&label=Views)](https://github.com/alex6H/NER-Location-extraction-and-geocoding)

> Extracts structured location information from unstructured incident text using a local LLM, geocodes results, and visualizes them on a Folium map. Designed to keep sensitive text processing local while using pluggable geocoders (Google Maps, OSM/Nominatim, etc.).

This script automates the extraction and visualization of location information from unstructured text, particularly focusing on security incidents in conflict zones. It utilizes a local Large Language Model (LLM) to ensure privacy while extracting location details from sensitive text, which are then formatted for submission to a geocoding system. 

Google Maps is employed in this implementation, but users can configure and use an in-house OpenStreetMap geocoding system or any other for enhanced privacy and autonomy. The resulting locations are plotted on an interactive map using Folium, facilitating comprehensive visual analysis. This workflow enables users to process sensitive data locally, addressing privacy concerns and providing detailed geographical insights for informed decision-making.

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

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [LMStudio](https://lmstudio.ai/) for providing local LLM capabilities
- [Hugging Face](https://huggingface.co/) for hosting the language models
- [Folium](https://python-visualization.github.io/folium/) for mapping capabilities
- The open-source community for various geocoding solutions

## Support

- **Issues**: [GitHub Issues](https://github.com/alex6H/NER-Location-extraction-and-geocoding/issues)
- **Discussions**: [GitHub Discussions](https://github.com/alex6H/NER-Location-extraction-and-geocoding/discussions)

---

⭐ **Star this repository if you find it helpful!**
