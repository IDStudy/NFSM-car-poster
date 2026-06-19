## 📥 下载方式

### 方案一：浏览器下载 ZIP（无需 Git，推荐）

打开仓库页面，点绿色 **Code** 按钮 → **Download ZIP**，解压后海报在 `车辆海报/` 文件夹里。

> 自行删除无关文件即可，最简单。

---

### 方案二：Git Clone 完整克隆

适合装了 Git 的玩家，后续更新方便：

点绿色 **Code** 按钮，在「克隆」分区确认选中 **HTTPS** 标签（不要选 SSH 或 GitHub CLI），复制链接：

```
https://github.com/IDStudy/NFSM-car-poster.git
```

在终端执行：

```bash
git clone https://github.com/IDStudy/NFSM-car-poster.git
```

执行后完整仓库自动拉取到本地。以后有新车上架，在仓库目录里运行：

```bash
git pull
```

增量拉取，只下载新增/更新的文件。

---

### 方案三：Git 稀疏检出（仅下载海报文件夹）

不想拉完整仓库，只要 `车辆海报/` 里的图片：

```bash
mkdir car-poster && cd car-poster
git init
git remote add origin https://github.com/IDStudy/NFSM-car-poster.git
git config core.sparseCheckout true
echo "车辆海报/" >> .git/info/sparse-checkout
git pull origin main
```

执行完后 `car-poster/车辆海报/` 里就是全部海报图片，不包含其他文件和历史。
