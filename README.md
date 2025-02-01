# Run Ollama
Ref: https://hub.docker.com/r/ollama/ollama

### CPU Only
```
docker run -d --restart always -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

### Run Ollama dgn GPU
Harus diinstall dulu Nvidia Container Toolkit package

```
docker run -d --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

### Run Ollama dengan GPU AMD

```
docker run -d --device /dev/kfd --device /dev/dri -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama:rocm
```

### Bisa langsung dipakai dari shell dengan:

```
docker exec -it ollama ollama run llama3
```



# Run Open-WebUI
Ref: https://github.com/open-webui/open-webui

### CPU Only

```
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

### Run Open-WebUI dgn GPU Nvidia

```
docker run -d -p 3000:8080 --gpus all --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:cuda
```



# download model llama3.2 dan deepseek-r1

```
https://ollama.com/library
```



### Xenara Cafe and Coworking Space
Ruko Citra Grand, Blok London C-08, Semarang, Jawa Tengah, Indonesia
