FROM mcr.microsoft.com/windows/servercore:ltsc2022

EXPOSE 11434

ENV OLLAMA_HOST=0.0.0.0
ENV OLLAMA_MODELS='C:\models'

COPY ./nvdll/* C:/Windows/
COPY ./ollama-windows-amd64 C:/app

WORKDIR C:/app
ENTRYPOINT ollama.exe serve
