
## Prerequisites

- Docker
- Docker Compose
- Up to date NVIDIA drivers
- NVIDIA Container Toolkit

## Getting Started

1. Clone this repository:
   ```
   git clone <repository-url>
   cd <project-directory>
   ```

2. Build and run the Docker container:
   ```
   docker-compose up --build
   ```

3. Once the container is running, you'll see a URL in the console output that looks like:
   ```
   http://127.0.0.1:8888/lab?token=<some_long_token>
   ```
   Copy and paste this URL into your web browser.

4. In the Jupyter Lab interface, open `diffusion_model_pipeline.ipynb`.

5. Run the cells in the notebook to perform data acquisition, analysis, and preparation, and to train the baseline model.

## Stopping the Container

To stop the Docker container, use `Ctrl+C` in the terminal where you ran `docker-compose up`, or run `docker-compose down` in another terminal in the same directory.

