# Split directories of data into training and test sets

Say we have a directory containing three sub-directories, and want to randomly split this into training and test datasets.

```
existing_data
├── apples
│   ├── apples1
│   ├── apples2
│   ├── apples3
│   ├── apples4
│   ├── apples5
│   ├── apples6
│   ├── apples7
│   └── apples8
├── bananas
│   ├── bananas1
│   ├── bananas2
│   ├── bananas3
│   ├── bananas4
│   ├── bananas5
│   ├── bananas6
│   ├── bananas7
│   └── bananas8
└── oranges
    ├── oranges1
    ├── oranges2
    ├── oranges3
    ├── oranges4
    ├── oranges5
    ├── oranges6
    ├── oranges7
    └── oranges8

```

And we want to split these categories into training and test directories.

```python
train_test_split_dir(source="existing_data", destination="new_data_split")
```

```
new_data_split
├── test
│   ├── apples
│   │   ├── apples1
│   │   └── apples6
│   ├── bananas
│   │   ├── bananas1
│   │   └── bananas4
│   └── oranges
│       ├── oranges1
│       └── oranges5
└── train
    ├── apples
    │   ├── apples2
    │   ├── apples3
    │   ├── apples4
    │   ├── apples5
    │   ├── apples7
    │   └── apples8
    ├── bananas
    │   ├── bananas2
    │   ├── bananas3
    │   ├── bananas5
    │   ├── bananas6
    │   ├── bananas7
    │   └── bananas8
    └── oranges
        ├── oranges2
        ├── oranges3
        ├── oranges4
        ├── oranges6
        ├── oranges7
        └── oranges8

```


```python
train_test_split(source, destination, test_prop)
```

**Note** the data is copied.