FROM mcr.microsoft.com/windows/servercore:ltsc2022

EXPOSE 11434

ENV OLLAMA_HOST=0.0.0.0 OLLAMA_MODELS='C:\models'

COPY ./nvdll/System32 C:/Windows/System32
COPY ./nvdll/SysWOW64 C:/Windows/SysWOW64
COPY ./ollama-windows-amd64 C:/app

WORKDIR C:/app
ENTRYPOINT ollama.exe serve
