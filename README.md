Docker image to play TensorRT technology with AUTOMATIC1111's web ui.
Docker image: kopyl/a1111-tensorrt

### Features:

- Speed of image generation is ≈75it/s for Stable Diffusion 1.5
- You can run it from [Runpod](https://runpod.io/gsc?template=lschv5bdvp&ref=0xwirw9o). [Video tutorial](https://youtu.be/MPD4OBWD_So)

### Requirements for Runpod:

- Expose ports: 8888, 3000
- Reserve disk space: 100 GB for contaier volume
- Configure right GPU: NVIDIA RTX 4090

### Metadata:

- NVIDIA driver: 535.104.12
- CUDA driver: 11.8
