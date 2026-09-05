# Solusi: tantangan-instalasi

Pelajaran: [Tantangan: pasang tmux di mesin sendiri](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-instalasi)

Buktikan tmux hidup di mesin yang **kamu** pakai setiap hari.

## 1. Versi

```bash
tmux -V
```

Harus menampilkan versi (contoh: `tmux 3.4`). Kalau `command not found`:

| OS | Perintah |
|---|---|
| macOS (Homebrew) | `brew install tmux` |
| Ubuntu / Debian / WSL | `sudo apt update && sudo apt install -y tmux` |
| Fedora | `sudo dnf install -y tmux` |

Jangan install tmux di PowerShell Windows — pakai WSL.

## 2. Sesi `produksi` dengan program yang masih hidup

```bash
tmux new -s produksi
```

Di dalam sesi, pilih salah satu yang ada di mesinmu:

```bash
top
# atau: python3
# atau: node
# atau: watch -n 1 date
```

Detach: `Ctrl+b` lalu `d`. **Tutup** jendela terminal.

## 3. Terminal baru, attach

```bash
tmux ls
# produksi: 1 windows (...)

tmux attach -t produksi
```

`top` / `watch` / interpreter masih jalan — itu bukti sesi tidak mati saat jendela terminal ditutup.

Hapus sesi setelah selesai: `tmux kill-session -t produksi`.
