## Kill Process

```bash
sudo kill -s 9 $(ps aux | grep 'node' | grep -v grep|  awk '{print $2}')
```

```bash
sudo kill `pgrep vim`
```

## Fork Bomb

> Detail: https://linux.cn/article-5685-1.html

```bash
:(){:|:&};:
```
