# Tree-Based Models: Random Forests

## Objective
I compared a random forest with a single decision tree and linear models on California Housing and measured which features drive its predictions.

## Methodology
- I split California Housing into 16,512 training rows and 4,128 test rows and fitted a single decision tree, OLS, Ridge and a random forest.
- I scored each model by RMSE and R² on the training rows and the test rows, and read the forest's out-of-bag score.
- I measured the forest's feature importance two ways: impurity (MDI) and permutation importance on the test rows.
- I tuned max_depth and max_features with 3-fold cross-validation and scored the tuned forest on the test rows.
- I wrote my own prompt asking an AI for a function that charts permutation importance and returns it as a table, and checked its numbers against mine.

## Key Findings
- The single tree had a test R² of 0.6228, Ridge had 0.5758 and the random forest had 0.8046.
- Latitude scored 0.0890 by MDI but 0.4427 by permutation, so the two measures rank the features differently.
- The tuned forest reached a test R² of 0.8094.
- My AI function took 2 rounds, and every line of the check said yes, matching my permutation numbers in every printed digit.
