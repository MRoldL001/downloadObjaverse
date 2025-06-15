<div align="left">
  <img src="dlobj-title.png" alt="TITLE" width="700">
</div>

Stable download of the Objaverse dataset under poor network conditions

在较差的网络环境下稳定下载 Objaverse 数据集

## ✅ 优势
- 该脚本在下载过程中会持续重试，确保指定的数据集完整下载完毕，不会因网络不稳定而中断下载
- 脚本通过两个 `.txt` 文件维护下载进度，支持随时手动中断和恢复。你可以在任意时刻停止下载，之后再次运行脚本即可从上次中断处继续
    - 此外，强制中断后生成的 `done.txt` 文件记录了已成功下载的数据集列表，你可以据此查看当前本地已有的资源
- ~开发者喜欢岛田美波，善善~

## 🚀 快速开始
> [!IMPORTANT]
> 请提前组织 `.json` 文件
>
> **仅支持 dict 和 list 两种组织形式**

> [!TIP]
> 下载路径由 ai2 研究所提供的 `objaverse` Pathon Package 维护，在 dict 中将希望存放的路径指定为键或值不会改变预设的下载路径

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
