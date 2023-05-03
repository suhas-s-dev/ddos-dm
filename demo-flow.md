## Before
### Cleanup Mininet Topology
```
sudo mn -c
```

### Remove Old results
```
rm -rf *.csv && rm -rf *.png
```

## Data Collection Mode

### Terminal 1 - Normal Traffic Controller
```
ryu-manager train_normal.py
```

### Terminal 2 - Normal Traffic Generator
```
sudo python3 topo_normal.py && sudo mn -c
```

### Terminal 1 - Attack Traffic Controller
```
ryu-manager train_attack.py
```

### Terminal 2 - Attack Traffic Generator
```
sudo python3 topo_attack.py && sudo mn -c
```

## Detection & Mitigation Mode

### Terminal 1 - Normal Traffic Controller
```
ryu-manager mitigate_normal.py
```

### Terminal 2 - Normal Traffic Generator
```
sudo python3 topo_normal.py && sudo mn -c
```

### Terminal 1 - Attack Traffic Controller
```
ryu-manager mitigate_attack.py
```

### Terminal 2 - Attack Traffic Generator
```
sudo python3 topo_attack.py && sudo mn -c
```