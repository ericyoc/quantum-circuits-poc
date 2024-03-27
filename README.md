# Quantum Image Classification using PennyLane

This repository contains a Python script that demonstrates quantum image classification using the PennyLane library and the MNIST dataset. The script creates a quantum circuit using the `default.qubit` device provided by PennyLane and applies a variational classifier to predict the digit represented in a given test image.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Quantum Circuit](#quantum-circuit)
- [Variational Classifier](#variational-classifier)
- [Results](#results)
- [Quantum Platform Comparison](#quantum-platform-comparison)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites
To run this script, you need to have the following prerequisites installed:
- Python (version 3.6 or higher)
- PennyLane library
- NumPy library
- Matplotlib library (for visualizing the circuit)

## Installation
1. Clone this repository:
   ```
   git clone https://github.com/your-username/quantum-image-classification.git
   ```

2. Install the required libraries:
   ```
   pip install pennylane numpy matplotlib
   ```

## Usage
1. Navigate to the cloned repository:
   ```
   cd quantum-image-classification
   ```

2. Run the script:
   ```
   python quantum_image_classification.py
   ```

   The script will load the MNIST dataset, create a quantum circuit using PennyLane, and apply a variational classifier to predict the digit represented in a test image. The predicted digit will be printed in the console.

## Quantum Circuit
The quantum circuit used for image classification is defined in the `circuit` function. It takes the flattened and scaled input image and encodes it into the quantum circuit using RX gates. The `StronglyEntanglingLayers` template is then applied to the circuit, followed by measurements of the expectation values of the Pauli-Z operator on each qubit.

## Variational Classifier
The variational classifier is defined in the `variational_classifier` function. It takes the weights and bias as input and returns a classifier function. The classifier function applies the quantum circuit to the input image and computes the dot product of the circuit outputs with the weights, adding the bias term.

## Results
The script predicts the digit represented in a test image from the MNIST dataset using the variational classifier. The predicted digit is printed in the console.

Additionally, the script visualizes the quantum circuit using the `qml.draw_mpl` function from PennyLane and saves the circuit diagram as `pennylane_circuit.png`.

## Quantum Platform Comparison
The following table compares various quantum computing platforms and their capabilities:

| Quantum Company | Quantum AI Platform | Quantum AI Language | Quantum AI Summary | Quantum Computer | Public Access | Simulated or Actual | Classical-Quantum Hybrid Functionality | Dependencies | Total Qbits | Usage Pros | Usage Cons | Quantum Hardware Types |
|-----------------|---------------------|---------------------|--------------------|-----------------------|---------------|---------------------|----------------------------------------|--------------|-------------|------------|------------|------------------------|
| Amazon Braket | PennyLane | Python | A cross-platform Python library for quantum machine learning, automatic differentiation, and optimization of hybrid quantum-classical computations. | Various (IonQ, Rigetti, D-Wave) | Yes | Both | Yes | Python 3.7+, PennyLane 0.28.0+, NumPy 1.20.0+ | [11, 5000+] | Integration with AWS, access to multiple quantum hardware providers, seamless integration with classical machine learning frameworks | Requires an AWS account and credits, limited to supported quantum hardware providers | Superconducting qubits, Trapped ions, Quantum annealers |
| IBM Quantum | Qiskit | Python | An open-source quantum computing framework for programming quantum computers, with a focus on quantum circuits. | IBM Quantum Experience | Yes | Both | Yes | Python 3.7+, Qiskit 0.37.0+ | 127 | Large community, extensive documentation, access to real quantum hardware, integration with classical Python libraries | Limited quantum hardware availability, requires knowledge of quantum circuits and algorithms | Superconducting qubits |
| Google | Cirq | Python | An open-source framework for writing, manipulating, and optimizing quantum circuits and running them on quantum computers and simulators. | Google Sycamore | No | Both | Yes | Python 3.7+, Cirq 1.1.0+ | 53 | Intuitive and user-friendly API, extensive documentation and tutorials, supports both simulation and execution on real quantum hardware | Limited access to Google's quantum hardware, primarily focused on gate-based quantum computing | Superconducting qubits |
| Microsoft Azure Quantum | Q# | Q# (C# integration) | A domain-specific programming language used for expressing quantum algorithms and integrating them with classical code in the .NET environment. | Various (IonQ, Honeywell, QCI) | Yes | Both | Yes | N/A | [11, 32] | Seamless integration with the .NET ecosystem, access to multiple quantum hardware providers through Azure, extensive documentation and tutorials | Requires familiarity with the .NET framework and C#, limited community compared to Python-based frameworks | Superconducting qubits, Trapped ions |

This comparison table provides additional information about the quantum platforms, including their associated quantum programming languages, quantum computers, public access availability, simulation and actual hardware capabilities, classical-quantum hybrid functionality, dependencies, total qubits, usage pros and cons, and supported quantum hardware types.

## Contributing
Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).
