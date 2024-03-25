Make sure that you have python 3.10 or later installed 
>>python --version

Open this folder in any code editor

Activate the virtual environment
>>.\env\Scripts\activate

Install the requirements in the active virtual environment using pip:
>>python -m pip install -r requirements.txt

Copy the example.env template into .env
>>cp example.env .env

I am using the https://huggingface.co/TheBloke/Nous-Hermes-13B-GGML/blob/main/nous-hermes-13b.ggmlv3.q4_K_M.bin model here. The model is relatively large (7.82 GB) but the results are on par with GPT3.5

Download all the models
>>python download_models.py

If you get an output that says "LLM model downloaded and ready!", the setup was completed successfully

Ingesting the documents
>> python ingest.py

Running privateGPT
>> python privateGPT.py
-------------------------------------------------------------------------------------------------------------
Troubleshooting


Python Version
To use this software, you must have Python 3.10 or later installed. Earlier versions of Python will not compile.

ModuleNotFoundError on Windows
Depending on your installation of Python, you may need to use py or python to run the different scripts. If one of the two fails with ModuleNotFoundError, try the other one.


C++ Compiler
If you encounter an error while building a wheel during the pip install process, you may need to install a C++ compiler on your computer.

For Windows 10/11
To install a C++ compiler on Windows 10/11, follow these steps:

Install Visual Studio 2022.
Make sure the following components are selected:
Universal Windows Platform development
C++ CMake tools for Windows
Download the MinGW installer from the MinGW website.
Run the installer and select the gcc component.

