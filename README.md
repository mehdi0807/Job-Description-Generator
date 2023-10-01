# Job-Description-Generator
This GitHub repository showcases a project focused on creating a job description generator using state-of-the-art text-to-text models. Leveraging the power of Hugging Face's pre-trained models, specifically `Flan-t5-base`. This project aims to automate the process of generating job descriptions based on role-specific information.
## Dataset
The dataset, which is accessible at [https://www.kaggle.com/datasets/andrewmvd/data-scientist-jobs/data], comprises a collection of over 3900 job listings tailored specifically for data scientist positions. Originally created by picklesueat, this dataset encompasses a rich array of attributes, including salary estimates, geographical location, detailed job descriptions, and more. Its inception was to serve as a resource facilitating projects dedicated to job market analysis and salary prediction.

As part of my project, I performed preprocessing on this dataset to refine it to ensure that the dataset aligns seamlessly with the task of fine-tuning text-to-text models requirements and objectives.
## Preprocessing
In the preprocessing phase, the dataset underwent a series of strategic transformations to make it conducive for training text-to-text models, specifically targeting the task of job description generation. The following key steps were undertaken:

- To align the dataset with the text-to-text model's input-output format, each job listing was meticulously transformed into a `prompt` and an `answer`. The `prompt` encapsulated the role-specific information, such as job title, location, company sector, and any other relevant details, serving as the basis for generating job descriptions. The `answer` component, on the other hand, encapsulated the actual job description text that the model aimed to generate.
- A data cleaning process was executed to remove any inconsistencies, errors, or irrelevant information from the dataset. This step ensured that the models learned from a better quality data.
- To optimize model performance and streamline the training process, a decision was made to retain only the shortest job descriptions from the dataset.
## Limitaions
- The model was fine-tuned solely on data science jobs, limiting its effectiveness outside this domain.
- Due to GPU constraints, a small batch size (2) was used, potentially affecting training stability.
- The model was trained for only 10 epochs due to time constraints, potentially hindering full model convergence.
- Model may struggle with longer, more complex job descriptions.
- Pretrained models may introduce bias from their original training data, affecting generated content fairness and accuracy.
## System specefications
- Python version : `3.11.3`
- System : `Microsoft Windows 11 (64-bit)`
- Processor : `11th Gen Intel Core(TM) i5 11400H @2700H`
- GPU : `NVIDIA GeForce GTX 1050`
- RAM : `16 GB`
