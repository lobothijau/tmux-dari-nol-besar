# Solusi: tantangan-detach

Pelajaran: [Tantangan: sesi yang selamat dari disconnect](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-detach)

Proses di dalam tmux tetap hidup setelah jendela terminal ditutup — pola yang sama dipakai saat SSH putus.

## Langkah

```bash
tmux new -s detach-latihan
```

Di dalam sesi:

```bash
sleep 600
# alternatif visual: watch date
```

Detach: `Ctrl+b` lalu `d`. Tutup jendela terminal sepenuhnya.

Buka terminal baru:

```bash
tmux ls
tmux attach -t detach-latihan
```

`sleep` masih berjalan (belum kembali ke prompt). Cek dari pane/window lain atau terminal di luar tmux:

```bash
tmux list-panes -t detach-latihan -F "#{pane_current_command}"
# sleep
```

atau:

```bash
ps aux | grep "[s]leep 600"
```

## Detach vs exit

- `Ctrl+b d` — keluar dari sesi, proses **tetap** jalan
- `exit` / `Ctrl+d` di shell terakhir — sesi **mati**, `sleep` ikut berhenti

Hapus sesi: `tmux kill-session -t detach-latihan`.
