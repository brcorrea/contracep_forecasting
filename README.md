## Forcasting of contraceptive demand in Cote d'Ivory


### Dataset: 

Contraceptive consumption of 11 contraceptive products in 156 health services in Cote d'Ivory from Jan-2016 until Jun-2019.

* Data: data/Train.csv

* Metadata: data/Table_of_Contents.xlsx


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
