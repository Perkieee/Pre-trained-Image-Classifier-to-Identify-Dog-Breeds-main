# Dog Breed Image Classifier
This project focuses on classifying images of dogs into specific breeds, utilizing machine learning to distinguish between dog and non-dog images. The classifier leverages pre-trained Convolutional Neural Network (CNN) models to identify accurately whether an image contains a dog and, if so, predict its breed. The primary goal is to assess the model's ability to correctly classify dog breeds.
## Project Overview
The project processes and classifies images using a selected CNN model (ResNet, AlexNet, VGG). Several functions are implemented to facilitate image classification, result evaluation, and performance summarization:

*Image Classification:* Applies the chosen CNN model to label each image.

*Label Comparison:* Compares the true pet image labels with the model’s predictions.

*Dog Identification:* Verifies if the labels correspond to dogs, helping evaluate accuracy for both dog and non-dog classifications.

## Key Files

*classifier.py:* Contains the pre-trained CNN model used for classifying images.

*adjust_results4_isadog.py:* Determines if the predicted labels represent dogs, using a predefined list of dog breeds.

*calculates_results_stats.py:* Computes key performance metrics (e.g., accuracy, precision) for dog and non-dog classifications.

*dognames.txt:* A list of dog breed names used to verify if predicted labels represent dog breeds.

## Project Workflow

*get_input_args:* Retrieves and parses three command-line arguments the user provides when running the program. If any argument is missing, default values are applied:

Image folder: --dir (default: pet_images)
CNN model architecture: --arch (default: vgg)
Dog names text file: --dogfile (default: dognames.txt)

*get_pet_labels:* Creates a dictionary (results_dic) of pet labels based on image filenames.

*classify_images:* Processes images using the CNN model and stores the classification results in a dictionary with filenames as keys.

*adjust_results4_isadog:* Updates the dictionary by checking if each pet and classifier label represents a dog.

*calculates_results_stats:* Evaluates the classification results and computes performance metrics, such as accuracy for dog and non-dog classifications.

## Running the Project

To run the project, execute the run_models_batch.sh script from the terminal. This script runs check_images.py three times, once for each CNN model, and stores the results in their respective .txt files.

You can also test additional images by preprocessing them and then executing run_models_uploaded_batch.sh to classify them using the pre-trained models.
