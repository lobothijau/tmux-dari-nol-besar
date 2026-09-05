# Solusi: tantangan-pane

Pelajaran: [Tantangan: layout coding dua pane](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-pane)

Satu window, dua pane vertikal: editor kiri, jalankan file kanan. Pindah antar pane tanpa mouse.

`file.py` di folder ini adalah contoh minimal.

## Layout

```bash
tmux new -s pane-coding
```

Split vertikal: `Ctrl+b` lalu `%`.

- Pane kiri (aktif setelah split biasanya kanan — pindah dengan `Ctrl+b` lalu panah kiri):

  ```bash
  nano file.py
  # atau editor yang kamu pakai: vim file.py
  ```

- Pane kanan:

  ```bash
  python3 file.py
  # atau: npm test  (kalau proyek Node)
  ```

Pindah pane: `Ctrl+b` lalu tombol panah. Jangan pakai mouse untuk tantangan ini.

## Shortcut

| Setelah `Ctrl+b` | Aksi |
|---|---|
| `%` | Split vertikal (kiri \| kanan) |
| `"` | Split horizontal (atas / bawah) |
| panah | Pindah pane |
| `x` | Tutup pane aktif (konfirmasi `y`) |
| `z` | Zoom pane (fullscreen sementara) |

Hapus sesi: `tmux kill-session -t pane-coding`.
