```python
import numpy as np

def calculate(list):
    if len(list) != 9:
        raise ValueError("List must contain nine numbers.")
    
    matrix = np.array(list).reshape(3, 3)
    
    mean_axis1 = matrix.mean(axis=0).tolist()
    mean_axis2 = matrix.mean(axis=1).tolist()
    mean_flat = matrix.mean().tolist()

    variance_axis1 = matrix.var(axis=0).tolist()
    variance_axis2 = matrix.var(axis=1).tolist()
    variance_flat = matrix.var().tolist()

    stddev_axis1 = matrix.std(axis=0).tolist()
    stddev_axis2 = matrix.std(axis=1).tolist()
    stddev_flat = matrix.std().tolist()

    max_axis1 = matrix.max(axis=0).tolist()
    max_axis2 = matrix.max(axis=1).tolist()
    max_flat = matrix.max().tolist()

    min_axis1 = matrix.min(axis=0).tolist()
    min_axis2 = matrix.min(axis=1).tolist()
    min_flat = matrix.min().tolist()

    sum_axis1 = matrix.sum(axis=0).tolist()
    sum_axis2 = matrix.sum(axis=1).tolist()
    sum_flat = matrix.sum().tolist()

    calculations = {
        'mean': [mean_axis1, mean_axis2, mean_flat],
        'variance': [variance_axis1, variance_axis2, variance_flat],
        'standard deviation': [stddev_axis1, stddev_axis2, stddev_flat],
        'max': [max_axis1, max_axis2, max_flat],
        'min': [min_axis1, min_axis2, min_flat],
        'sum': [sum_axis1, sum_axis2, sum_flat]
    }
    
    return calculations
```
