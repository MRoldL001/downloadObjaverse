# downloadObjaverse.py
Stable download of the Objaverse dataset under poor network conditions

在较差的网络环境下稳定下载 Objaverse 数据集

## 🚀 快速开始
> [!IMPORTANT]
> 请提前组织 `.json` 文件
>
> 仅支持 dict 和 list 两种组织形式

```bash
wget https://raw.githubusercontent.com/MRoldL001/downloadObjaverse/main/downloadObjaverse.py
pip install objaverse
python downloadObjaverse.py --json_path <your_json_path>
```

## 🧭 参数说明
> [!TIP]
> `todo.txt` 和 `done.txt` 被用来维护下载进度，为了方便后续操作，默认在下载完成后是保留的，可以加参数 `-d` 或者长参数 `--delete` 来在数据集全部下载完成后删除

| 参数 | 用途 |
|------|------|
| `--json_path` | JSON 文件(下载列表)的路径 |
| `--todo_path` | 生成 todo.txt 的路径，默认与脚本在同一目录下 |
| `--done_path` | 生成 todo.txt 的路径，默认与脚本在同一目录下 |
| `-d` `--delete` | 在全部下载完成后删除 todo.txt 与 done.txt |
| `-h` `--help` | 显示帮助信息 |
