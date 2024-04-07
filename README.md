# pokemon-gan
Neural Network project for designing a GAN for generating new Pokémon

# Dataset
Both dataset and trained models can be found [here](https://drive.google.com/drive/u/0/folders/1SJEGvdh2vwAm5BLvq6jvsvOkNq9GOdBD).

# Setup
#### Local machine
Use requirements.txt to run `data_augmentation.ipynb` and `model_evaluation.ipynb` notebooks on your local machine.
#### Cloud service
You will need a cloud service like [Saturn Cloud platform](https://saturncloud.io/) in order to run `gan.ipynb` and `classifier.ipynb`. It is essential to create required directories:
- When running `gan.ipynb`, you should have the following directory structure:
```
root/
│
├── gan.ipynb                   # Jupyter notebook containing DCGAN implementation
├── trained_models/             # Folder to store trained models
├── generated_images/           # Folder to store generated images 
└── dataset/                    # Folder containing dataset used for training 
    │
    ├── gen_{generation_no}/    # Nested folder containing specific generation images
    │   ├── 151_0_9727.png      # Image 1
    │   ├── 151_0_6487.png      # Image 2
    │   └── ...                 # Other images
```
- When running `classifier.ipynb`, you should have the following directory structure (batches contain 500 images generated from each DCGAN specialized for a single generation):
```
root/
│
├── classifier.ipynb            # Jupyter notebook containing DCGAN implementation
└── dataset/                    # Folder containing dataset used for training 
    │
    ├── batch_1                 # Nested folder containing images from first batch
    │   ├── image-0_gen_1.png   # Image 1
    │   ├── image-0_gen_1.png   # Image 2
    │   └── ...                 # Other images
    ├── batch_2                 # Nested folder containing images from second batch
    │   └── ...                 
    ├── batch_4                 # Nested folder containing images from third batch
    │   └── ...                 
    ├── batch_4                 # Nested folder containing images from fourth batch
    │   └── ...                 
```
