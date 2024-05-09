# Initial Results

| Model                   | Concepts | Assertions|
| :-----------------------| :------: | :--------:|
| 2010 State of the Art   |  0.852   |   0.936   |
| SciBERT                 |  0.849   |   0.783   |
| BioBERT                 |  0.848   |   0.773   |
| Traditional BERT        |  0.820   |   0.737   |

## Hyperparameters
Learning Rate                     = 2e-5;
Weight Decay                      = 1e-2;        
Epochs (with Early Stopping)      = 20

## Next Steps
Hyperparameter tuning on learning rate, weigth decay, and number of epochs

## Scaled Model
The best performing model for concept recognition, SciBERT, was retrained on 80% of training data, or 341 discharge notes, and achieved an F1 of 0.881, which is 3.4% larger than the F1 of the winning model in the 2010 challenge (0.852). 

In contrast, the original training dataset from the challenge was 73 discharge notes, where 7 of these notes were used for validation. The change in training size was a factor of ~5, and training time increased from ~12 minutes to ~40 minutes. 

Note: hyperparameters were held constant across all models (see section "Hyperparameters")
