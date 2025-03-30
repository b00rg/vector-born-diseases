# Vector-Borne Disease Vector Identification Using Neural Networks
Vector-borne diseases are responsible for over 700,000 deaths annually, accounting for more than 17% of all infectious diseases. This project leverages image recognition through Neural Networks to identify harmful vectors, such as insects and arachnids, that may carry diseases. By recognizing key morphological features of these vectors, we can differentiate between disease-carrying species and non-harmful animals.

### Project Overview:
The goal of this project is to accurately identify different genera of disease-carrying vectors (e.g., mosquitoes, ticks, and kissing bugs) based on visual features. For example, distinguishing an Anopheles mosquito (known for its characteristic striped body) from a common mosquito (which typically has a plain brown body). This project utilizes neural networks to analyze images and classify various species of disease vectors, enabling quicker detection and response to potential disease outbreaks.

### Trained Animals/Species:
The neural network is trained to identify and classify the following vectors:
1. Anopheles mosquito
2. Aedes mosquito
3. Culex mosquito
4. Various genera of ticks (including Lone Star tick and Black-legged tick)
5. Blackfly
6. Triatoma (also known as the kissing bug)

### Key Features Recognized:
1. Body Morphology: Identifying characteristic body markings, such as striped patterns in Anopheles mosquitoes.
2. Anatomical Positioning: Analyzing the positioning and structure of body parts to distinguish between species.
3. Comparative Analysis: Contrast between vectors and non-harmful animals based on visual characteristics.

### Tools & Libraries Used:
This project is implemented in Python and utilizes the following libraries:
- TensorFlow and Keras: For building and training the neural network models.
- NumPy: For numerical operations and data manipulation.
- skimage: For image processing and feature extraction.
- PIL (Python Imaging Library): For handling image input/output and augmentation.
- Web Scraping: To gather large datasets of vector images for training.
- Image Augmentation: To enhance the dataset and increase model robustness.

### How It Works:
1. Data Collection: Web scraping techniques are employed to gather large datasets of vector and non-vector images.
2. Data Preprocessing: Images are processed and augmented to improve the model's ability to generalize.
3. Model Training: A convolutional neural network (CNN) is used to train the model to recognize distinguishing features of different vectors.
4. Prediction & Classification: The trained model classifies incoming images as either harmful vectors or non-harmful animals.
