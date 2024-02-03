# TO-DOs/Tasks:
### CNN:
1. [✅] Use masks to normalize brain data
2. [ ] Train-test split
    - [ ] Randomly split participants: 520 training, ~104 validation & hypertuning, ~132 testing
        - Control for age and sex across splits ()
3. [ ] Implement Model
    - 3 layers (fully-connected), 2 hidden layers: ~30 & ~20 neurons each (w/ ReLU)
    - Output layer trained with softmax given pixels from segs_refs
4. [ ] Evaluate CNN performance with Dice Score (dice_coef)?
    - ![alt text](dice_formula.png)
5. [ ] Use Statistics and/or machine learning to identify relationship with participant age
    - Correlation, (non)-linear reggression, mutual formation, etc.