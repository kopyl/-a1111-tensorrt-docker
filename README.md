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

### When this can be useful:

- When you reuse one or some set of Stable Diffusion models a lot (not suitable for one-time generation)
- When you generate a lo of images for your videos (it's suitable cause when you save 1± second per image, it's a lot of time for like 2-3 minutes video)

### Are there any other ways to speed up image generation?

- Convert SD model to fp16
- Use Oneflow (it's tricky, cause without any modification of the source code of the library you're going to get a huge cold start, so the speed evens out and also you can't use it with A1111, since it's Diffusers-like tech)

### How to contribute:

- You can freeze current commit of repositories (A1111 and TensorRT extension)
- You can add a serverless Dockerfile and a handler for Runpod
