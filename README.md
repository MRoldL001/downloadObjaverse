<div align="left">
  <img src="dlobj-title.png" alt="TITLE" width="700">
</div>

Stable download of the Objaverse dataset under poor network conditions

在较差的网络环境下稳定下载 Objaverse 数据集

## ✅ 优势
- 该脚本直到指定的数据集被全部下载完成前会一直重试，不存在因为网络不稳定而中止下载的可能

- 用两个 ´.txt´ 文件维护下载进度，你可以随时手动中断下载，然后在某个时刻再次运行该脚本以继续下载

    - 因为上述特性，你也可以在强制中断后得到一份当前在电脑中存在的数据集的列表，即文件 ´done.txt´

- ~开发者喜欢岛田美波，善善~

## 🚀 快速开始
> [!IMPORTANT]
> 请提前组织 `.json` 文件
>
> **仅支持 dict 和 list 两种组织形式**

```bash
wget https://raw.githubusercontent.com/MRoldL001/downloadObjaverse/main/downloadObjaverse.py
pip install objaverse
python downloadObjaverse.py --json_path <your_json_path>
```

## 🧭 参数说明
> [!TIP]
> `todo.txt` 和 `done.txt` 被用来维护下载进度，为了方便后续操作，默认在下载完成后是**保留**的，可以加参数 `-d` 或者长参数 `--delete` 来在**数据集全部下载完成后删除**

| 参数 | 用途 |
|------|------|
| `--json_path` | JSON 文件(下载列表)的路径 |
| `--todo_path` | 生成 todo.txt 的路径，默认与脚本在同一目录下 |
| `--done_path` | 生成 todo.txt 的路径，默认与脚本在同一目录下 |
| `-d` `--delete` | 在全部下载完成后删除 todo.txt 与 done.txt |
| `-h` `--help` | 显示帮助信息 |
