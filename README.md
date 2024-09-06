# SDXL v0.9 in Docker 🐋

```
export HUGGINGFACE_TOKEN=<my huggingface token>
```
```
docker build -t sdxl:v0.9 --build-arg HUGGINGFACE_TOKEN=$HUGGINGFACE_TOKEN .
```
```
mkdir -p outputs
```
```
docker run -ti --gpus all \
    -v $PWD/outputs:/outputs \
    -e OUTPUT_DIR=/outputs/ \
    -e PROMPT="a lilypad on a galaxy of water" \
     stable-diffusion-xl:latest
```
Will overwrite `outputs/image0.png` each time.
