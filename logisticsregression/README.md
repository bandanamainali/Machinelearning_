#  Logistic Regression 
##  what is logistic Regression ??
 Logistic regression is a supervised machine learning algorithm widely used for binary classification tasks, such as identifying whether an email is spam or not and diagnosing diseases by assessing the presence or absence of specific conditions based on patient test results.

🔹 df[['age']]
This is selecting the "age" column as a DataFrame.

Double square brackets [[...]] are used to keep the result as a DataFrame instead of a Series.

If you used df['age'], you'd get a Series (a single column, 1D), but models expect X (features) to be in 2D format, even if it's just one column.

✅ df[['age']] → shape: (n, 1) → correct for input features

🔹 df.bought_insurance
This selects the target/output label — whether the insurance was bought or not.

Single bracket (or dot notation) gives you a Series, which is fine for the y (labels).

✅ df.bought_insurance → shape: (n,) → correct for output labels

🔹 train_test_split(...)
This function splits the data into training and testing sets. You're giving it:

X: df[['age']] → input feature(s)

y: df.bought_insurance → target

train_size=0.9 → 90% of the data will go into training, 10% into testing

It returns:

X_train, X_test: features for training/testing

y_train, y_test: corresponding labels

these four variables will get assigned as:

X_train → 90% of the feature data (df[['age']])

X_test → remaining 10% of the feature data

y_train → 90% of the target data (df.bought_insurance)

y_test → remaining 10% of the target data

