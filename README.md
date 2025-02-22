# Genesis Tutorial

## 参考

- [Genesisの公式ドキュメント](https://genesis-world.readthedocs.io/en/latest/index.html)
- [GenesisのGitHub](https://github.com/Genesis-Embodied-AI/Genesis)
- [誰かのQiita](https://qiita.com/hEnka/items/cc5fd872eb0bf7cd3abc)

## 0. 注意事項

- GPUを使うことが前提
- Linux環境でないと描画ができない(Windowsでは学習のみできる)
- Anacondaはインストール済みであること

## 1. 環境構築

```bash
conda create -n genesis-tutorial python=3.11
conda activate genesis-tutorial
```

## 2. ライブラリインストール

### 2.1. PyTorch

公式ページからインストール

<url>https://pytorch.org/</url>
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

### 2.2. その他のライブラリ

```bash
pip install genesis-world
git clone https://github.com/Genesis-Embodied-AI/Genesis.git
git clone https://github.com/leggedrobotics/rsl_rl
cd rsl_rl && git checkout v1.0.2 && pip install -e .
pip install tensorboard
```

## 3. Train

```bash
python Genesis/examples/locomotion/go2_train.py
```

## 4. Evaluation

linuxの場合
```bash
python Genesis/examples/locomotion/go2_eval.py
```

windowsの場合

mujocoを用いて描画
```bash
python sim2sim/go2_eval_mujoco.py
```




