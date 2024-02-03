# TO-DOs/Tasks:

### Realistic :D
1. Find number of GM, WM, & CSF pixels for each participant
    - Voxel Brightness values: CSF = 1, GM = 2, WM = 3
2. Feed into ML classifier (i.e., LR) and label with ages
    - Find relationship between GM, WM, & CSF with age



### CNN: (NOW A STRETCH GOAL!)
1. [✅] Use masks to normalize brain data
2. [ ] Find Ground Truth Data
     - Voxel Brightness values: CSF = 1, GM = 2, WM = 3
3. [ ] Train-test split
    - [ ] Randomly split participants: 520 training, ~104 validation & hypertuning, ~132 testing
        - Control for age and sex across splits ()
4. [ ] Implement Model
    - 3 layers (fully-connected), 2 hidden layers: ~30 & ~20 neurons each (w/ ReLU)
    - Output layer trained with softmax given pixels from segs_refs
5. [ ] Evaluate CNN performance with Dice Score (dice_coef)?
    - ![alt text](dice_formula.png)
6. [ ] Use Statistics and/or machine learning to identify relationship with participant age
    - Correlation, (non)-linear reggression, mutual formation, etc.