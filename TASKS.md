# TO-DOs/Tasks:
### CNN:
1. Train-test split
    - Randomly split participants: 520 training, ~104 validation & hypertuning, ~132 testing
        - Control for age and sex across splits ()
    - Evaluate with Dice Score (dice_coef)?
        - 2 * (|pred_pixels * intersecting_pixels * |) / (|| + ||)
