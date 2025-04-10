# inear regression of single variable

## house price prediction relative to area.

### Save model using Pickle
Pickle allows you to serialize machine learning models in their existing state, making it possible to use them again as needed. In this section, we will learn to serialize a machine learning model with Pickle. Great! The parameters of the model we just unpickled are the same as the one we initially created.


# what is serialization in python ??
Serialization is the process of converting a Python object into a byte stream or a string representation that can be easily stored or transmitted. The serialized form preserves the object's structure and internal data. In Python, the built-in pickle module provides the functionality to perform serialization.

Why use pickle in Python?
pickle is a module in Python used to save and load Python objects.

Think of it like this:

You have a Python object (like a list, dictionary, or even your custom class).

You want to store it in a file or send it over a network.

But Python objects can’t be saved directly in their original form.

So, you use pickle to convert (serialize) the object into a byte stream (a format that can be saved or transferred).

Later, you can load (deserialize) it back into the same Python object.

🔹 What is Serialization?
Serialization is the process of:

Converting a Python object into a byte stream (or string format) that can be stored or transferred.

Example:

python
Copy
Edit
import pickle

data = {"name": "Bandana", "role": "Professor"}

# Serialize (save) the object to a file
with open("data.pkl", "wb") as f:
    pickle.dump(data, f)
🔹 What is Deserialization?
Deserialization is the reverse process:

Converting the stored byte stream back into a Python object.

Example:

python
Copy
Edit
# Load the object back
with open("data.pkl", "rb") as f:
    loaded_data = pickle.load(f)

print(loaded_data)  # Output: {'name': 'Bandana', 'role': 'Professor'}
🔸 In Simple Words:
Serialization = Save the object (convert to bytes)

Deserialization = Load the object back (convert to original)


 