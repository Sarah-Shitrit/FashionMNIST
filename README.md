# FashionMNIST
 The goal is to compare different regularizations: weight decay, dropout and batch nornalization with one another and with LENET-5 without regularization. The criterion for comparison is the accuracy.
 
## General explanation:
The notebook is divided into 5 sections: Imports and downloads, Networks, Train and save data of best models. Load and test trained networks’ parameters and plots and accuracy table.

**Imports and downloads**: here we define the path to the location in which we would like to save the models’ parameters / the location in which they are saved in case we only want to use existing parameters without re-training the model. We also import sine modules and create the dataloaders.

**Networks**: Building the architecture of the models. There are 3 blocks, each for one model: LENET-5 without regularization & LENET-5 with weight decay (same model since the weight decay is defined through the optimizer later on), LENET-5 with dropout, and lastly, LENET-5 with batch normalization.

**Train and save data of best models**: There are 4 code blocks under this markdown. Each block trains one of the networks and saves the model’s parameters that achieved the highest accuracy when tested on the test set. The files will be saved in the folder that was defined as the parameter “models_path”.

**Load and test trained networks’ parameters**: The first 4 code-blocks loads the parameters of pre-trained networks. Attention! All blocks will save the model with the trained parameters under the variable “model”, therefore models should be loaded and tested one at a time. The 5th code-block is testing the model over a batch of 64 examples from the test set. After running the block, the accuracy for that batch will be printed.

**Plots and accuracy table**: first 2 code-blocks import some modules and load the accuracies that were calculated during the training of the models. The next 4 code-blocks produce convergence graphs. The last block produces the accuracy table.

## Train the models:
1.	Important! Change the value of the parameter “models_path” to the path of where you want the models’ parameters to be saved. “models_path” appears at the first block. 
2.	Run all blocks under the markdown “ Imports and downloads”
3.	Run all of the blocks under the markdown “Networks”.
4.	Run all blocks under the markdown “Train and save data of best models”.

## Test the models with saved weights:
1.	Change the parameter “models_path” value to the path in which the models’ parameters are saved. “models_path” appears at the first block. 
2.	Run all blocks under the markdown “ Imports and downloads”
3.	Run all of the blocks under the markdown “Networks”.
4.	Under the markdown “Load and test trained networks' parameters” run firstly one of the loading blocks (the first 4 code-blocks) in order to load the parameters of a desired model. Then, run the last (5th) code block in order to test that model. Attention! There is a need to load one model, then test it, and only after that load another model for test. Do not try to load all the model’s data at the same time, unless giving each model a different name. For example: run the blocks under this markdown in that sequence to test all the models: 1,5,2,5,3,5,4,5.
5.	Run all blocks under the markdown “ Plots and Accuracy table”
