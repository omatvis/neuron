# Glossary

Short definitions used in this repository.

- **Neural network (NN):** A model made of layers that apply linear transformations and nonlinear activation functions to map inputs to outputs.
- **Model:** The function (with parameters/weights) that produces an output (prediction) given an input.
- **Weights / parameters:** The values inside a model that are learned during training.
- **Inference:** Using a model (usually already trained) to produce predictions from inputs. In this repo, `POST /predict` is the inference endpoint.
- **Training:** The process of adjusting weights to reduce prediction error on a dataset. In this repo, `POST /train` is the training endpoint (Phase 2+).
- **Dataset:** A collection of input/output examples used for training or evaluation.
- **Loss (loss function):** A numeric measure of how wrong the model’s predictions are. Training tries to minimize loss.
- **Gradient:** The direction and rate of change of the loss with respect to model weights. Used to update weights.
- **Optimizer:** The algorithm that updates weights using gradients (e.g., gradient descent, Adam).
- **Epoch:** One full pass over the training dataset.
- **Overfitting:** When a model performs well on training data but poorly on new/unseen data.
- **XOR problem:** A tiny dataset/task (often 2 inputs → 1 output) that demonstrates why a neural network may need a hidden layer to learn non-linear patterns.