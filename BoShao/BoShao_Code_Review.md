# ML Leaks
Use Python 3.10  
1. When running ```pip install -r requirements.txt```, meet:
```
ERROR: Could not find a version that satisfies the requirement bitsandbytes==0.44.1 (from versions: 0.31.8, 0.32.0, 0.32.1, 0.32.2, 0.32.3, 0.33.0, 0.33.1, 0.34.0, 0.35.0, 0.35.1, 0.35.2, 0.35.3, 0.35.4, 0.36.0, 0.36.0.post1, 0.36.0.post2, 0.37.0, 0.37.1, 0.37.2, 0.38.0, 0.38.0.post1, 0.38.0.post2, 0.38.1, 0.39.0, 0.39.1, 0.40.0, 0.40.0.post1, 0.40.0.post2, 0.40.0.post3, 0.40.0.post4, 0.40.1, 0.40.1.post1, 0.40.2, 0.41.0, 0.41.1, 0.41.2, 0.41.2.post1, 0.41.2.post2, 0.41.3, 0.41.3.post1, 0.41.3.post2, 0.42.0)
ERROR: No matching distribution found for bitsandbytes==0.44.1
```
The requirements.txt file is NOT correct.
2. We need to try the models ourselves. His code does not save any models or report any results in the intermediate process.
3. The code only reports and member/non-member accuracy on the test dataset, and the accuracy is less than 50% (49.53%). So the MIA attack fails accorrding to the accuracy.  

# BadNet
Use Python 3.10
1. numpy meets version conflict
```
A module that was compiled using NumPy 1.x cannot be run in NumPy 2.0.0 as it may crash. To support both 1.x and 2.x versions of NumPy, modules must be compiled with NumPy 2.0. Some module may need to rebuild instead e.g. with 'pybind11>=2.12'.

If you are a user of the module, the easiest solution will be to downgrade to 'numpy<2' or try to upgrade the affected module. We expect that some modules will need time to support NumPy 2.
```
Fix numpy
```
pip uninstall numpy
pip install "numpy<2.0"
```
2. We need to try the models ourselves. His code does not save any models or report any results in the intermediate process.
3. He only reports the prediction accuracy on the poisoned test dataset, no any other results. So only based on the output of his code, we cannot decide if his attack is success.
