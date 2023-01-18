# Zero-shot-finetuning-transformers
 Zero-shot-finetuning-transformers


## What can you do?

- You can create custom classification dataset 
- You can push your custom dataset to huggingface hub
- You can fine-tune any model on your custom dataset (zero-shot), classification task
- You can evaluate your model on your custom dataset
- You can use your model for inference

## How to use?

- Install requirements

  ```commandline
  pip install -r requirements.txt
  ```

### 1. Create custom dataset

- I am using daya source from various sources. In 'data_generator' folder, you can find the datasets from individual sources.

- I have created 'data_generator/script.py' file which will create a single dataset from all the individual datasets.

- This produces 'data_generator/train.csv' file which is the final dataset. This will be further used by 'dataset_generator.py' file to create dataset according to huggingface format and push dataset to huggingface hub.

- You can add your own dataset but it should be in the same format as 'data_generator/train.csv' file.

- You can check 'data.py' file. If you want you can add examples in it. Do not change the format of the examples.


- > NOTE: ABOVE STEPS ARE OPTIONAL. YOU CAN SKIP. I have already created a dataset 'dataset_generator/train.csv' file.

- Below command will create huggingface dataset and push it to huggingface hub.

    ```commandline
    python dataset_generator.py
    ```
  
- This will create a dataset in 'dataset_folder' folder. This is final dataset.


### 2. Push your dataset to huggingface hub

- You can push your dataset to huggingface hub. You can check the dataset in huggingface hub.

    ```commandline
    python push_to_hub.py
    ```
  
- This will push your dataset to huggingface hub. You can check the dataset in huggingface hub.

### 3. Fine-tune any model on your custom dataset (zero-shot), classification task

- You can fine-tune any model on your custom dataset (zero-shot), classification task. You can check the dataset in huggingface hub.

    ```commandline
    python zero-shot-finetuning-train.py
    ```
  
  or

- You can also check out jupyter notebook 'zero-shot-finetuning-train.ipynb' for more details.
  
- This will fine-tune any model on your custom dataset (zero-shot), classification task. You can check the dataset in huggingface hub.

- This will also save the model and push to huggingface hub.

- You can check the model in huggingface hub.


### 4. Inference

- It is recommended to open the script 'inference.py' and change the model name and dataset name to your model and dataset name.

- Run the script 'inference.py' to get the inference.

    ```commandline
    python inference.py
    ```
  

## How to contribute?

- You can contribute to this repository by adding more examples in 'data.py' file. 

- You can contribute to this repository by adding more datasets in 'data_generator' folder. 

- Make sure to follow the format of 'data_generator/train.csv' file. And also make sure to add the dataset merger code if required in 'data_generator/script.py' file.

## References

https://github.com/huggingface/setfit/blob/main/notebooks/zero-shot-classification.ipynb

https://github.com/jianguoz/Few-Shot-Intent-Detection/tree/main/Datasets/HWU64

https://www.kaggle.com/datasets/elvinagammed/chatbots-intent-recognition-dataset

## Thanks me on-
Follow me on Instagram: https://www.instagram.com/dipesh_pal17

Subscribe me on YouTube: https://www.youtube.com/dipeshpal17

Donate me: https://www.buymeacoffee.com/dipeshpal
