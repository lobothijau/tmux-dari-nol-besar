# tmux dari Nol — final

Konfigurasi lengkap Modul 7–8 kelas [tmux dari Nol](https://kodepas.com/kelas/tmux-dari-nol-besar): mouse, history, key binding, copy-mode vi, dan status bar sederhana.

Prefix tetap `Ctrl+b`. Plugin TPM tidak disertakan — ubah sedikit, tes, baru tambah.

## Prasyarat

- Terminal (macOS, Linux, atau WSL)
- tmux terpasang — `tmux -V`

## Pasang

```bash
git clone https://github.com/kodepas/tmux-dari-nol-besar.git
cd tmux-dari-nol-besar
git checkout final
cp .tmux.conf ~/.tmux.conf
tmux source-file ~/.tmux.conf
```

## Binding yang ditambah

| Setelah prefix `Ctrl+b` | Aksi |
|---|---|
| `r` | Reload `~/.tmux.conf` |
| `|` | Split vertikal di direktori pane aktif |
| `-` | Split horizontal di direktori pane aktif |

Copy mode (vi): `Ctrl+b [` lalu `v` pilih, `y` salin, `q` keluar. Paste: `Ctrl+b ]`.

## Bandingkan dengan starter

```bash
git diff starter final -- .tmux.conf
```
