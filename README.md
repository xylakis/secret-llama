# secret-llama

Chat with open-source language models without sending your conversations to a remote inference service. secret-llama is a TypeScript browser LLM chatbot that runs Llama 3, Mistral, and other supported models on your computer through WebGPU.

## Features

- Keep conversation data on your computer with local, in-browser inference.
- Run supported models through [WebLLM](https://github.com/mlc-ai/web-llm), without a separate inference server.
- Chat offline after the application and model files have been downloaded and cached.
- Choose from models such as TinyLlama, Llama 3, Phi 1.5, and Mistral.
- Use a browser chat interface without installing a desktop application.

**Check WebGPU support first.** You need a compatible browser and GPU. Chrome and Edge are options; support in other browsers depends on their version and configuration. Model memory requirements vary. The donor lists model downloads from roughly 600 MB for TinyLlama to 4.3 GB for Llama 3; download size is not the same as runtime memory use.

## Installation

For a local build, install Node.js and Yarn, download or clone this project's source, and open its directory:

```sh
cd secret-llama
yarn
yarn build-and-preview
```

This builds the React application and starts a local preview. The local web server delivers the application; model inference still runs in your browser.

The following command assumes the standalone repository is hosted at `secret-llama/secret-llama` and publishes a `secret-llama-v0.1.0.tar.gz` release asset. That release location is a distribution convention, not a verified existing download; adjust it to the actual repository and asset name before use.

```sh
curl -fL https://github.com/secret-llama/secret-llama/releases/download/v0.1.0/secret-llama-v0.1.0.tar.gz -o secret-llama-v0.1.0.tar.gz
```

## Usage

For development with live reload:

```sh
yarn dev
```

For a Vite-based development setup, you can pass a local bind address and port through the development script:

```sh
yarn dev --host 127.0.0.1 --port 5173
```

Open the URL printed by the development server, select a model, and wait for its initial download before sending a message. Choose a smaller model if your device cannot load a larger one.

**The first load needs a network connection.** Offline use depends on the application and model files remaining available in your browser's cache. Clearing browser storage may require another download.

## License

Licensed under Apache-2.0. This project is based on [abi/secret-llama](https://github.com/abi/secret-llama). Preserve applicable copyright, license, and attribution notices when redistributing the source or modified versions.

## Related projects

The following repositories were supplied as other tools from the same author. Their purposes were not included in the source material, so they are listed without inferred feature descriptions:

- [sifat-zporter/network_scanner](https://github.com/sifat-zporter/network_scanner): consult its README for its scope and usage.
- [pmamediajogja-cyber/gantryd](https://github.com/pmamediajogja-cyber/gantryd): consult its README for its scope and usage.
- [rachmathidayat2021/prometheus](https://github.com/rachmathidayat2021/prometheus): consult its README for its scope and usage.

