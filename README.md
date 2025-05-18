
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

4. In the Jupyter Lab interface, open `best_models_new.ipynb`.

5. Run the cells in the notebook to perform data acquisition, preparation, training and evaluation.

## Stopping the Container

To stop the Docker container, use `Ctrl+C` in the terminal where you ran `docker-compose up`, or run `docker-compose down` in another terminal in the same directory.

## Most important notebooks

The most important notebooks are the following:

- best_models_new.ipynb: The full pipeline of our best findings on a limited set of features, from data preparation to training our best (gradient boosting and forest based) models and evaluating them.
- best_models_all_features.ipynb: The full pipeline of our best findings on all of the generated features, otherwise the same as the previous file.
- dl_best_models.ipynb: Training of a feedforward net with the best hyperparametres found in a WandB sweep.

## Other notebooks

- data_prep.ipynb: Data preparation, profiling and visualization
- feature_engineering.ipynb: Feature engineering, but with a few mistakes that have been corrected since
- baseline_model_comparison.ipynb: Experimentation with different models: training and evaluation (bad performances beacuse of minmax scaling in features). 
- DeepLearning.ipynb: Contains the Wandb sweep for the feedforward net
- top_models_opt.ipynb: Optimization of the best gradient boosting and forest based models.
- investigation.ipynb: Investigation of the cause of the bad performance (we found the min-max scaling that was the root of the problem.)

The rest of the files are .html files from the data profiling and .png images from model comparison and feature importances.
