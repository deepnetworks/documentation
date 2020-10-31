# Practical PyTorch documentation

### Optimizer hyperparameters
#### `Adam`
- Adam uses momentum.

#### `RMSprop`
- RMSprop does not include momentum.

#### `SGD`

### Common operations

#### Computing softmax

The `dim` parameter of the `F.softmax` function determines which axis to normalize. So, if your data is `(n_batches, n_classes)`, then you want to use `dim=1`, since you're normalizing over the classes.

#### Freezing weights

```python
for param in model.parameters():
    pass
```

#### Run one optimization step

```python
for input_data, target in dataset:
    optimizer.zero_grad()
    output = model(input_data)
    loss = loss_fn(output, target)
    loss.backward()
    optimizer.step()
```

#### Print (all) the gradient values for a network
```python
for param in model.parameters():
    print(param.grad)
```

#### Gather values at specific indices in a matrix
```python
indices
gathered = torch.gather(input_data, dim=1, indices)
```