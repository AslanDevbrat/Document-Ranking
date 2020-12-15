
# Document Ranking with AllenNLP
## Note: 
In this project I have used Configuration files for the training, that means you will not find a jupyter notebook for the training insted there is a .jsonnet file which conatin all this, like number of epoch, learning rate, optimizers, dropout ...., do check that [file](https://github.com/AslanDevbrat/Document-Ranking/blob/master/experiments/mimics.jsonnet)
## Usage

First way (Recommended)

- Create a new notebook in google Colab. Make sure you have selelcted the GPU as Hardware accelarator
- Then clone my [Github Repository](https://github.com/AslanDevbrat/Document-Ranking.git) using this command `!git clone "https://github.com/AslanDevbrat/Document-Ranking.git"`
- Now change the directory using `% cd Document-Ranking`
- Now use following command to install library with correct compatible version 

  

      !pip install allennlp==1.2.0
      !pip install transformers==3.1.0

### Data

Run `python scripts/data_split.py "https://github.com/microsoft/MIMICS/raw/master/data/MIMICS-ClickExplore.tsv"` to automatically download the dataset to your `/tmp/` directory.

### Training

Then, install the remaining dependencies:

```shell
pip install -r requirements.txt
```

Then:

```shell
allennlp train experiments/mimics.jsonnet -s /tmp/your_output_dir
```

## YOU don't have to worry much. Everything is written in the Run-Me.iypnb file, You just have to rull all cells in google colab.


