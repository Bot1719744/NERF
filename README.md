# Tiny ZipNeRF Project

## Purpose of the Project
The purpose of this project is to enhance the **Tiny NeRF (Neural Radiance Fields)** model by implementing **Tiny ZipNeRF**, which introduces a grid-based feature representation and adaptive sampling techniques. These improvements result in faster training and rendering, higher frame rates for video rendering, and enhanced detail in visual outputs. Tiny ZipNeRF is optimized for applications requiring efficient real-time or near-real-time 3D rendering.

---

## Instructions for Setting Up the Environment and Running the Code

### 1. Clone the Repository
```bash
git clone <repository-link>
cd Tiny-ZipNeRF
```

### 2. Set Up the Python Environment
Excecute first two section in the ipynb file named tiny_nerf.ipynb.

### 3. Install Dependencies
Install all required packages following Dependencies and Installation Instructions below.

### 4. Running the Code
To run Tiny ZipNeRF, execute the ipynb file named tiny_nerf.ipynb:


---

## Dependencies and Installation Instructions

This project requires the following dependencies:
- **TensorFlow** >= 2.5: For model building and training.
- **NumPy**: For numerical operations.
- **OpenCV**: For potential post-processing of rendered images.
- **Matplotlib**: For visualizing outputs and performance metrics.
- **Imageio**: For creating videos from rendered frames.

---

## Module and Script Descriptions

- **tiny_zipnerf.py**: This single file handles the entire Tiny ZipNeRF pipeline, including data loading, model initialization, training, and rendering. Within this script:
  - **Data Loading**: Loads and preprocesses images and camera poses.
  - **Model Initialization**: Sets up the grid-based feature representation and adaptive sampling.
  - **Training**: Runs the training loop with PSNR tracking.
  - **Rendering**: Produces a rendered output and computes metrics such as temporal consistency and high-frequency content.

---

## Special Considerations and Known Issues

1. **Rendering Artifacts**: If temporal inconsistencies appear in video rendering (e.g., flickering), consider adjusting the multisampling density or `N_samples` to improve frame stability.

2. **Memory Consumption**: The grid-based representation requires additional memory, especially for larger grid sizes. Reducing `grid_size` may help manage memory usage without significantly impacting quality.

3. **Compatibility**: The code is optimized for TensorFlow 2.x. Compatibility issues may arise with TensorFlow 1.x or other deep learning frameworks.

4. **Performance Optimization**: Tiny ZipNeRF is designed for high-performance rendering, but the specific setup (e.g., GPU/CPU configuration) can significantly impact rendering times.

---

## Dataset Submission

The dataset used for this project should be a set of 2D images of a scene and the corresponding camera poses. The data should follow the following structure:
Thank you for the clarification. Here’s an updated README tailored to the single-file setup: