Save pth
=======================
- [Save by yourself](#Save_by_yourself)

## Save_by_yourself
```python
# change the name, for saving multiple files
model_name = 'model.net'

checkpoint = {'n_hidden': net.n_hidden,
              'n_layers': net.n_layers,
              'state_dict': net.state_dict(),
              'tokens': net.chars}

with open(model_name, 'wb') as f:
    torch.save(checkpoint, f)
    
    
#load
# Here we have loaded in a model that trained over 20 epochs `rnn_20_epoch.net`
with open('model.net', 'rb') as f:
    checkpoint = torch.load(f)
    
loaded = CharRNN(checkpoint['tokens'], n_hidden=checkpoint['n_hidden'], n_layers=checkpoint['n_layers'])
loaded.load_state_dict(checkpoint['state_dict'])
```

