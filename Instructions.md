Project Execution Instructions

This project performs wafer defect classification using a trained ONNX model and a Python-based inference pipeline. Follow the steps below to run the project successfully.

System Requirements

• Operating System: Windows / Linux / macOS
• Python Version: 3.8 or higher
• Hardware: CPU sufficient (no GPU required)

Step 1: Clone or Download the Repository

Download the project repository from GitHub or extract the provided ZIP file.

Ensure the following files are present in the root directory:
• EDGE_AI_MODEL_Final.ipynb
• semiconductor_defect_model.onnx
• semiconductor_defect_model.onnx.data
• dataset folder (sample images)

Step 2: Set Up the Python Environment

Create and activate a virtual environment (recommended):

python -m venv edge_ai_env
source edge_ai_env/bin/activate      (Linux / macOS)
edge_ai_env\\Scripts\\activate       (Windows)


Install required dependencies:

pip install numpy opencv-python onnx onnxruntime torch torchvision matplotlib pillow


Step 3: Prepare Input Images

• Use grayscale wafer inspection images
• Place images inside the dataset/test/ folder
• Organize images by defect class if using batch testing
• Images must be resized to 224 × 224 during preprocessing

Note: Grayscale images are automatically replicated to 3 channels during preprocessing.

Step 4: Run the Model Using Jupyter Notebook

Launch Jupyter Notebook:

jupyter notebook


Open the file:
EDGE_AI_MODEL_Final.ipynb

Execute all cells sequentially from top to bottom.

The notebook performs:
• Image preprocessing
• ONNX model loading
• Inference execution
• Prediction visualization

Alternative: Run ONNX Inference (Script-Based Logic)

If using a Python script instead of the notebook, the execution flow is:

• Load ONNX model using ONNX Runtime
• Preprocess input image (resize, normalize)
• Run inference
• Extract predicted defect class and confidence

Step 5: View Output

For each input image, the system outputs:
• Predicted defect category
• Confidence score
• Process-level insight where applicable

These outputs enable explainable and actionable defect analysis.

Troubleshooting

• Ensure ONNX and ONNX Runtime versions are installed correctly
• Verify image size and format before inference
• Confirm model file paths are correct
• Use Python 3.8+ to avoid compatibility issues

Deployment Note

The ONNX model is optimized for CPU-based edge deployment and can be integrated into production inspection pipelines or embedded devices with minimal modification.
