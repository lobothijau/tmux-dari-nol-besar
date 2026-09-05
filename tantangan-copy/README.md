# Solusi: tantangan-copy

Pelajaran: [Tantangan: salin error dari log](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-copy)

Salin satu baris error dari scrollback ke buffer tmux (atau clipboard), tanpa screenshot.

`sample-log.txt` di folder ini mensimulasikan output tes yang gagal.

## Generate output panjang

```bash
tmux new -s copy-latihan
cat sample-log.txt
# atau: npm test
# atau: seq 1 80
```

## Copy mode (default tmux = keymap emacs)

1. `Ctrl+b` lalu `[` — masuk copy mode
2. Scroll ke baris error (panah, Page Up, atau `/` lalu ketik `Error` + Enter)
3. `Ctrl+Space` — mulai seleksi
4. Geser ke akhir baris
5. `Alt+w` atau `Ctrl+w` — salin ke buffer tmux (tmux 3.x: sering cukup `Enter`)
6. `q` — keluar copy mode jika masih di dalamnya
7. `Ctrl+b` lalu `]` — paste di pane yang sama atau pane lain

Kalau `setw -g mode-keys vi` sudah aktif (Modul 7):

1. `Ctrl+b` lalu `[`
2. `/Error` + Enter
3. `v` — mulai seleksi, `y` — yank
4. `q` keluar; paste dengan `Ctrl+b` lalu `]`

## Verifikasi

Paste di prompt atau di `nano`. Satu baris error (contoh: `Error: expected 200, got 500`) harus muncul utuh.

Hapus sesi: `tmux kill-session -t copy-latihan`.
