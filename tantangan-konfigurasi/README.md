# Solusi: tantangan-konfigurasi

Pelajaran: [Tantangan: tmux.conf starter](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-konfigurasi)

`tmux.conf` di folder ini adalah file minimal yang diminta tantangan: mouse, history panjang, dan satu key binding kustom.

## Pasang

```bash
cp tmux.conf ~/.tmux.conf
```

Reload tanpa restart sesi:

```bash
tmux source-file ~/.tmux.conf
```

atau di dalam tmux: `Ctrl+b` lalu `:` → `source-file ~/.tmux.conf` → Enter.

Kalau kamu sudah di cabang `starter`, cukup tambah binding `|` dan `r` ke `.tmux.conf` yang sudah ada, lalu reload.

## Verifikasi

Di dalam sesi tmux:

```bash
tmux show -g mouse
# mouse on

tmux show -g history-limit
# history-limit 50000
```

Lalu `Ctrl+b` lalu `|` — window terbagi vertikal. `Ctrl+b` lalu `r` menampilkan pesan reload.

Cabang `final` menambah status bar, index 1, dan copy-mode vi — itu Modul 7–8 secara utuh, lebih dari yang diminta tantangan ini.
