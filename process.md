## Kill Process

```bash
sudo kill -s 9 $(ps aux | grep 'node' | grep -v grep|  awk '{print $2}')
```
