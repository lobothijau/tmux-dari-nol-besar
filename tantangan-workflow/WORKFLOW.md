# Workflow tmux — contoh pribadi

Dokumentasi tantangan penutup. Sesuaikan; yang penting konsisten.

## Sesi

| Nama | Kapan | Layout |
|---|---|---|
| `learn` | Mengikuti kelas Kodepas | 1 window `kelas` — terminal untuk mengetik perintah pelajaran |
| `dev` | Kerja / side project | window `editor` + window `server` (pane kiri: proses/log, pane kanan: shell) |

## Perintah harian

```bash
# Pagi — lanjut sesi kemarin, atau buat kalau belum ada
tmux attach -t dev 2>/dev/null || tmux new -s dev
```

Di dalam `dev`:

1. Window 1 `editor` — editor atau shell di folder proyek
2. `Ctrl+b c`, rename `server`
3. `Ctrl+b |` — pane kanan untuk perintah ad-hoc; kiri jalankan server / `watch`

Sesi `learn` terpisah supaya catatan kelas tidak bercampur dengan proses deploy:

```bash
tmux new -s learn
tmux rename-window kelas
```

Pindah antar sesi (dari dalam tmux): `Ctrl+b s`.

## SSH / laptop ditutup

Detach dulu (`Ctrl+b d`), baru tutup terminal atau putuskan SSH. Attach lagi besok dengan `tmux attach -t dev`.

## Config

Isi `tmux.conf` di folder ini = cabang `final` (mouse, history 50000, binding `|` / `-` / `r`, copy-mode vi, status bar).
