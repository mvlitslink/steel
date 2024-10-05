# Pix2Pix Data Processing Pipeline

This project utilizes Pix2Pix for image-to-image translation and data processing with additional steps involving OmniGlue and template matching. Below is an overview of the steps involved in data processing, training, and troubleshooting common issues.

## Data Processing

The main data processing script is located in the `pix2pix_data` file. This script prepares the dataset for training by applying the following stages:

1. **Template Matching(deprecated):**
   - Initial data processing starts with template matching, which is used to align images or features within the dataset.
   
2. **OmniGlue Integration:**
   - The pipeline integrates **OmniGlue**, which helps with multi-modal data fusion. This step prepares the dataset for training the Pix2Pix model by combining different data representations into a coherent structure.(omniglue has issues with path so may need hacky code)

## Training with Pix2Pix

Once the data has been processed using the `pix2pix_data` script, it is ready for training. This project uses the Pix2Pix architecture, a popular choice for image-to-image translation tasks. Follow these steps to initiate the training process:

## Troubleshooting
If you encounter an error related to the auth_token parameter while fine-tuning the model, you can resolve this by deleting the auth_token parameter from the fine-tune file.