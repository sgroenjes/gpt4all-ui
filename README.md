# Gpt4All Web UI

![GitHub license](https://img.shields.io/github/license/nomic-ai/GPT4All-ui)
![GitHub issues](https://img.shields.io/github/issues/nomic-ai/GPT4All-ui)
![GitHub stars](https://img.shields.io/github/stars/nomic-ai/GPT4All-ui)
![GitHub forks](https://img.shields.io/github/forks/nomic-ai/GPT4All-ui)
[![Discord](https://img.shields.io/discord/1092918764925882418?color=7289da&label=Discord&logo=discord&logoColor=ffffff)](https://discord.gg/4rR282WJb6)

This is a Flask web application that provides a chat UI for interacting with [llamacpp](https://github.com/ggerganov/llama.cpp) based chatbots such as [GPT4all](https://github.com/nomic-ai/gpt4all), vicuna etc...

Follow us on our [Discord Server](https://discord.gg/4rR282WJb6).

Watch Install Video (Outdated, please use "New UI video") [Old Install Video](https://youtu.be/6kKv6ESnwMk)

Watch Usage Videos [Usage Video](https://youtu.be/DCBefhJUUh4)

Watch Settings Video [Settings Video](https://youtu.be/7KwR2vdt1t4)

Watch New UI Video [New UI + Install](https://youtu.be/M7NFajCyZKs)

![image](https://i.gyazo.com/ef94a5ac9169467a1aec228ef8c36c66.gif)

GPT4All is an exceptional language model, designed and developed by Nomic-AI, a proficient company dedicated to natural language processing. The app uses Nomic-AI's advanced library to communicate with the cutting-edge GPT4All model, which operates locally on the user's PC, ensuring seamless and efficient communication.

If you are interested in learning more about this groundbreaking project, visit their [Github Repository](https://github.com/nomic-ai/gpt4all), where you can find comprehensive information regarding the app's functionalities and technical details. Moreover, you can delve deeper into the training process and database by going through their detailed Technical report, available for download at [Technical report](https://s3.amazonaws.com/static.nomic.ai/gpt4all/2023_GPT4All_Technical_Report.pdf).

One of the app's impressive features is that it allows users to send messages to the chatbot and receive instantaneous responses in real time, ensuring a seamless user experience. Additionally, the app facilitates the exportation of the entire chat history in either text or JSON format, providing greater flexibility to the users.

It's worth noting that the model has recently been launched, and it's expected to evolve across time, enabling it to become even better in the future. This web UI is designed to provide the community with easy and fully localized access to a chatbot that will continue to improve and adapt across time.
# Features

- Chat with locally hosted AI inside a web browser
- Create, edit, and share your AI's personality
- Audio in and audio out with many options for language and voices (only Chrome web browser is supported at this time)
- History of discussion with resume functionality
- Add new discussion, rename discussion, remove discussion
- Export database to json format
- Export discussion to text format

# Installation and running

Make sure that your CPU supports `AVX2` instruction set. Without it, this application won't run out of the box. To check your CPU features, please visit the website of your CPU manufacturer for more information and look for `Instruction set extension: AVX2`.
> **Note**
>
>Default model `gpt4all-lora-quantized-ggml.bin` is roughly 4GB in size.

## Windows 10 and 11

### Automatic install

It is advised to have python 3.10 (The official one, not the one from Microsoft Store) and git installed. Although it should work with any python from 3.7, it is advised to use 3.10 to have the full support as some extensions like the future stable diffusion extension will force you to have 3.10.

1. [Go to the latest release section](https://github.com/nomic-ai/gpt4all-ui/releases)
2. Download the `webui.bat` if you are on windows or `webui.sh` if you are on linux/mac. but the download in a folder you name for example gpt4all-ui
3. Run the script and wait. It should install everything and start the chatbot
4. Before running, it may ask you to download a model. Feel free to accept or to download your own models depending on the backends you are using.

Once installed, you should see a new folder called GPT4All. From now on, you can run the app by using webui.bat or webui.sh. The script will check for any new updates
### Manual Simple install:

1. Download this repository .zip:

![image](https://user-images.githubusercontent.com/80409979/232210909-0ce3dc80-ed34-4b32-b828-e124e3df3ff1.png)

2. Extract contents into a folder.
3. Install/run application by double clicking on `webui.bat` file from Windows Explorer as normal user.

### Manual Advanced mode:

1. Install [git](https://git-scm.com/download/win).
2. Open Terminal/PowerShell and navigate to a folder you want to clone this repository.

```bash
git clone https://github.com/nomic-ai/gpt4all-ui.git
```

4. Install/run application by double clicking on `webui.bat` file from Windows explorer as normal user.

## Linux

### Automatic install

1. Make sure you have installed `curl`. It is needed for the one-liner to work.

`Debian-based:`
```
sudo apt install curl 
```
`Red Hat-based:`
```
sudo dnf install curl 
```
`Arch-based:`
```
sudo pacman -S curl 
```
2. Open terminal/console copy and paste this command and press enter: 
```
mkdir -p ~/gpt4all-ui && curl -L https://raw.githubusercontent.com/nomic-ai/gpt4all-ui/main/webui.sh -o ~/gpt4all-ui/webui.sh && chmod +x ~/gpt4all-ui/webui.sh && cd ~/gpt4all-ui && ./webui.sh
```
> **Note**
>
> This command creates new directory `/gpt4all-ui/` in your /home/ direcory, downloads a file [webui.sh](https://raw.githubusercontent.com/nomic-ai/gpt4all-ui/main/webui.sh), makes file executable and executes webui.sh that downloads and installs everything that is needed.

3. Follow instructions on screen until it launches webui.
4. To relaunch application: 
```
bash webui.sh
```

### Manual Simple install:

1. Download this repository .zip:

![image](https://user-images.githubusercontent.com/80409979/232210909-0ce3dc80-ed34-4b32-b828-e124e3df3ff1.png)

2. Extract contents into a folder.
3. Install/run application from terminal/console: 
```
bash webui.sh
```
### Manual Advanced mode:

1. Open terminal/console and install dependencies:

`Debian-based:`
```
sudo apt install curl git python3 python3-venv
```
`Red Hat-based:`
```
sudo dnf install curl git python3
```
`Arch-based:`
```
sudo pacman -S curl git python3
```

2. Clone repository:

```bash
git clone https://github.com/nomic-ai/gpt4all-ui.git
```
```bash
cd gpt4all-ui
```

3. Install/run application:

```bash
bash ./webui.sh
```

## MacOS

1. Open terminal/console and install `brew`:

```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install dependencies:

```
brew install git python3
```

3. Clone repository:

```bash
git clone https://github.com/nomic-ai/gpt4all-ui.git
```
```bash
cd gpt4all-ui
```

4. Install/run application:

```bash
bash ./webui.sh
```

On Linux/MacOS, if you have issues, refer to the details presented [here](docs/Linux_Osx_Install.md)
These scripts will create a Python virtual environment and install the required dependencies. It will also download the models and install them.

## Docker Compose
Make sure to put models the inside the `models` directory.
After that, you can simply use docker-compose or podman-compose to build and start the application:

Build
```bash
docker compose -f docker-compose.yml build
```

Start
```bash
docker compose -f docker-compose.yml up
```

Stop ` Ctrl ` + ` C `

Start detached (runs in background)
```bash
docker compose -f docker-compose.yml up -d
```

Stop detached (one that runs in background)
```bash
docker compose stop
```

After that, you can open the application in your browser on http://localhost:9600

Now you're ready to work!

# Supported backends
Two backends are now supported:
1 - [The llama_cpp backend](https://github.com/nomic-ai/pygpt4all)
2 - [The GPT-j backend](https://github.com/marella/gpt4all-j)
3 - Hugging face's Transformers (under construction)

# Supported models
You can also refuse to download the model during the install procedure and download it manually.

**For now, we support ggml models that work "out-of-the-box" (tested on Windows 11 and Ubuntu 22.04.2), such as:**

## LLama_cpp models
- [GPT4ALL 7B](https://huggingface.co/ParisNeo/GPT4All/resolve/main/gpt4all-lora-quantized-ggml.bin) or visit [repository](https://huggingface.co/ParisNeo/GPT4All)
- [GPT4ALL 7B unfiltered](https://huggingface.co/ParisNeo/GPT4All/blob/main/gpt4all-lora-unfiltered-quantized.new.bin) or visit [repository](https://huggingface.co/ParisNeo/GPT4All)
- [Vicuna 7B rev 1](https://huggingface.co/eachadea/legacy-ggml-vicuna-7b-4bit/resolve/main/ggml-vicuna-7b-4bit-rev1.bin) or visit [repository](https://huggingface.co/eachadea/legacy-ggml-vicuna-7b-4bit)  
- [Vicuna 13B rev 1](https://huggingface.co/eachadea/ggml-vicuna-13b-4bit/resolve/main/ggml-vicuna-13b-4bit-rev1.bin) or visit [repository](https://huggingface.co/eachadea/ggml-vicuna-13b-4bit)


## GPT-j models
- [GPT-j 7B](https://gpt4all.io/models/ggml-gpt4all-j.bin)

**These models don't work "out-of-the-box" and need to be converted to the right ggml type:**
## LLAMACPP models
- [Vicuna 7B](https://huggingface.co/eachadea/legacy-ggml-vicuna-7b-4bit/resolve/main/ggml-vicuna-7b-4bit.bin) or visit [repository](https://huggingface.co/eachadea/legacy-ggml-vicuna-7b-4bit)
- [Vicuna 13B q4 v0](https://huggingface.co/eachadea/ggml-vicuna-13b-1.1/resolve/main/ggml-vicuna-13b-1.1-q4_0.bin) or visit [repository](https://huggingface.co/eachadea/ggml-vicuna-13b-1.1/)
- [Vicuna 13B q4 v1](https://huggingface.co/eachadea/ggml-vicuna-13b-1.1/resolve/main/ggml-vicuna-13b-1.1-q4_1.bin) or visit [repository](https://huggingface.co/eachadea/ggml-vicuna-13b-1.1/)
- [ALPACA 7B](https://huggingface.co/Sosaka/Alpaca-native-4bit-ggml/resolve/main/ggml-alpaca-7b-q4.bin) or visit [repository](https://huggingface.co/Sosaka/Alpaca-native-4bit-ggml/)

Just download the model into the `models` folder and start using the tool.

# Build custom personalities and share them

To build a new personality, create a new file with the name of the personality inside the `personalities` folder. You can look at `gpt4all_chatbot.yaml` file as an example. Then you can fill the fields with the description, conditionning, etc. of your personality. Then save the file.

You can launch the application using the personality in two ways:
- Change it permanently by putting the name of the personality inside your configuration file
- Use the `--personality` or `-p` option to give the personality name to be used

If you deem your personality worthy of sharing, you can share the it by adding it to the [GPT4all personalities](https://github.com/ParisNeo/GPT4All_Personalities) repository. Just fork the repo, add your file, and do a pull request.

# Advanced Usage

If you want more control on your launch, you can activate your environment:

On Windows:
```cmd
env/Scripts/activate.bat
```

On Linux/MacOs:
```cmd
source venv/bin/activate
```

Now you are ready to customize your Bot.

To run the Flask server, execute the following command:
```bash
python app.py [--config CONFIG] [--personality PERSONALITY] [--port PORT] [--host HOST] [--temp TEMP] [--n_threads N_THREADS] [--n_predict N_PREDICT] [--top_k TOP_K] [--top_p TOP_P] [--repeat_penalty REPEAT_PENALTY] [--repeat_last_n REPEAT_LAST_N] [--ctx_size CTX_SIZE]
```

On Linux/MacOS more details can be found [here](docs/Linux_Osx_Usage.md)

## Options
*   `--config`: the configuration file to be used. It contains default configurations. The script parameters will override the configurations inside the configuration file. It must be placed in configs folder (default: default.yaml)
*   `--personality`: the personality file name. It contains the definition of the pezrsonality of the chatbot and should be placed in personalities folder. The default personality is `gpt4all_chatbot.yaml`
*   `--model`: the name of the model to be used. The model should be placed in models folder (default: gpt4all-lora-quantized.bin)
*   `--seed`: the random seed for reproductibility. If fixed, it is possible to reproduce the outputs exactly (default: random)
*   `--port`: the port on which to run the server (default: 9600)
*   `--host`: the host address at which to run the server (default: localhost). To expose application to local network, set this to 0.0.0.0.
*   `--temp`: the sampling temperature for the model (default: 0.1)
*   `--n_threads`: the number of threads to be used (default:8)
*   `--n-predict`: the number of tokens to predict at a time (default: 128)
*   `--top-k`: the number of top-k candidates to consider for sampling (default: 40)
*   `--top-p`: the cumulative probability threshold for top-p sampling (default: 0.90)
*   `--repeat-penalty`: the penalty to apply for repeated n-grams (default: 1.3)
*   `--repeat-last-n`: the number of tokens to use for detecting repeated n-grams (default: 64)
*   `--ctx-size`: the maximum context size to use for generating responses (default: 2048)

Note: All options are optional and have default values.

Once the server is running, open your web browser and navigate to http://localhost:9600 (or http://your host name:your port number if you have selected different values for those) to access the chatbot UI. To use the app, open a web browser and navigate to this URL.

Make sure to adjust the default values and descriptions of the options to match your specific application.

# Contribute

This is an open-source project by the community and for the community. Our chatbot is a UI wrapper for Nomic AI's model, which enables natural language processing and machine learning capabilities.

We welcome contributions from anyone who is interested in improving our chatbot. Whether you want to report a bug, suggest a feature, or submit a pull request, we encourage you to get involved and help us make our chatbot even better.

Before contributing, please take a moment to review our [code of conduct](./CODE_OF_CONDUCT.md). We expect all contributors to abide by this code of conduct, which outlines our expectations for respectful communication, collaborative development, and innovative contributions.

### Reporting Bugs

If you find a bug or other issue with our chatbot, please report it by [opening an issue](https://github.com/your-username/your-chatbot/issues/new). Be sure to provide as much detail as possible, including steps to reproduce the issue and any relevant error messages.

### Suggesting Features

If you have an idea for a new feature or improvement to our chatbot, we encourage you to [open an issue](https://github.com/your-username/your-chatbot/issues/new) to discuss it. We welcome feedback and ideas from the community and will consider all suggestions that align with our project goals.

### Contributing Code

If you want to contribute code to our chatbot, please follow these steps:

1.  Fork the repository and create a new branch for your changes.
2.  Make your changes and ensure that they follow our coding conventions.
3.  Test your changes to ensure that they work as expected.
4.  Submit a pull request with a clear description of your changes and the problem they solve.

We will review your pull request as soon as possible and provide feedback on any necessary changes. We appreciate your contributions and look forward to working with you!

Please note that all contributions are subject to review and approval by our project maintainers. We reserve the right to reject any contribution that does not align with our project goals or standards.

# Future Plans

Here are some of the future plans for this project:

**Enhanced control of chatbot parameters:** We plan to improve the UI of the chatbot to allow users to control the parameters of the chatbot such as temperature and other variables. This will give users more control over the chatbot's responses, and allow for a more customized experience.

**Extension system for plugins:** We are also working on an extension system that will allow developers to create plugins for the chatbot. These plugins will be able to add new features and capabilities to the chatbot, and allow for greater customization of the chatbot's behavior.

**Enhanced UI with themes and skins:** Additionally, we plan to enhance the UI of the chatbot to allow for themes and skins. This will allow users to personalize the appearance of the chatbot and make it more visually appealing.

We are excited about these future plans for the project and look forward to implementing them in the near future. Stay tuned for updates!

# License

This project is licensed under the Apache 2.0 License. See the [LICENSE](https://github.com/nomic-ai/GPT4All-ui/blob/main/LICENSE) file for details.
