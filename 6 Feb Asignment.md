Ans1)
```python
lst = [1,2,3,4, [44,55,66, True], False, (34,56,78,89,34), {1,2,3,3,2,1}, {1:34, "key2": [55, 67,78, 89], 4: (45,22, 61, 34)}, [56, 'data science'], 'Machine Learning']
```


```python
def product_of_numbers(lst):
    flat_list = list()
    for item in flat_list:
        if isinstance(item, (int, float)):
            flat_list.append(item)
        elif isinstance(item, list):
            flat_list.extend([i for i in item if isinstance(i, (int, float))])
        elif isinstance(item, tuple):
            flat_list.extend([i for i in item if isinstance(i, (int, float))])
        elif isinstance(item, dict):
            flat_list.extend([val for key, val in item.items() if isinstance(key, (int, float)) or all(isinstance(k, (int, float)) for k in key)])
            
product = 1
for num in flat_list:
    product *= num
    
print("Product", product)

```

    Product 362880



```python

```

