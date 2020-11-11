## Forcasting of Contraceptive Consumption in Cote d'Ivory Spotify


### Dataset: Contraceptive consumption of 11 products in XX cities on Cote d'Ivory from XX-2016 until XX-2020
Data: data/Train.csv
Metadata: data/Table_of_Contents.xlsx


### Build docker image to run the notebook

```
docker build -t contracep_forecasting_img .
```

### Run notebook server in docker

```bash
docker run -it --rm \
    -p 8888:8888 \
    -v $(pwd)/notebooks:/home/jovyan/notebooks \
    -v $(pwd)/data:/data/ \
    -v $(pwd)/plots:/plots/ \
    contracep_forecasting_img \
    jupyter notebook --notebook-dir /home/jovyan/notebooks
```
