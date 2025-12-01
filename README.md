
```markdown
# docker-hello-captain

A **beginner-friendly** demo repo that shows how I built my **first Docker image** and made it say hello.

## What I learnt here
1. Base image (`alpine:latest`) – the smallest Linux distro to start from.  
2. Dockerfile instructions – `FROM` and `CMD`.  
3. Building an image (`docker build`).  
4. Running a container (`docker run`).  
5. Environment variables – pass your name at runtime.

## Quick start
```bash
# 1. Clone (or download) this repo
git clone https://github.com/YOUR_GITHUB_USERNAME/docker-hello-captain.git
cd docker-hello-captain

# 2. Build the image
docker build -t hello-captain .

# 3. Run it
docker run hello-captain
# → Hello, Captain!

# 4. Pass your own name
docker run -e NAME=sumanth hello-captain
# → Hello, sumanth!
```

## Dockerfile explained (only 2 lines!)
```dockerfile
FROM alpine:latest          # start from a tiny Linux image
CMD echo "Hello, ${NAME:-Captain}!"  # print greeting; use NAME or default
```

That’s it—your first containerized “Hello World”.
```
