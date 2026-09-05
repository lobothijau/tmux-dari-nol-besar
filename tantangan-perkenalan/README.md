# Solusi: tantangan-perkenalan

Pelajaran: [Tantangan: sesi tmux pertama](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-perkenalan)

## Langkah

Buat sesi bernama `latihan`, jalankan satu perintah, detach, pastikan sesi masih ada, lalu attach lagi.

```bash
tmux new -s latihan
```

Di dalam sesi:

```bash
echo "tmux jalan"
```

Detach: `Ctrl+b` lalu `d` (bukan `exit` — `exit` menutup sesi).

Dari terminal biasa:

```bash
tmux ls
# latihan: 1 windows (...)

tmux attach -t latihan
# singkat: tmux a -t latihan
```

Teks `tmux jalan` masih ada di scrollback. Selesai.

## Kalau tersesat

| Gejala | Perbaikan |
|---|---|
| `duplicate session: latihan` | `tmux kill-session -t latihan` lalu ulangi, atau pakai nama lain |
| `no sessions` setelah detach | Kamu menekan `exit` / `Ctrl+d`, bukan `Ctrl+b d` |
| `Ctrl+b` tidak bereaksi | Pastikan status bar tmux terlihat di bawah layar |

Hapus sesi latihan setelah selesai: `tmux kill-session -t latihan`.
