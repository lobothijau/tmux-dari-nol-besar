# Solusi: tantangan-sesi-window

Pelajaran: [Tantangan: layout 3 window](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-sesi-window)

Satu sesi `tantangan`, tiga window bernama, detach tanpa kehilangan layout.

## Buat sesi dan window 0 (`shell`)

```bash
tmux new -s tantangan
```

Di dalam sesi, rename window aktif (`Ctrl+b` lalu `,`) menjadi `shell`, atau:

```bash
tmux rename-window shell
echo "window shell"
```

## Window `proses`

`Ctrl+b` lalu `c` untuk window baru, rename `proses`, lalu:

```bash
sleep 300
# atau: top
```

`sleep 300` menunggu 5 menit — cukup untuk bukti "masih jalan". Stop dengan `Ctrl+c` setelah verifikasi.

## Window `catatan`

`Ctrl+b` lalu `c` lagi, rename `catatan`, lalu:

```bash
echo "halo" > catatan.txt
# atau: nano catatan.txt
```

## Detach, cek, attach, loncat ke `proses`

`Ctrl+b` lalu `d`.

```bash
tmux ls
# tantangan: 3 windows (...)

tmux attach -t tantangan
```

Loncat ke window `proses`: `Ctrl+b` lalu `w`, pilih `proses` — atau `Ctrl+b` lalu nomor window-nya. `sleep` / `top` masih jalan.

## Shortcut yang dipakai

| Setelah `Ctrl+b` | Aksi |
|---|---|
| `,` | Rename window |
| `c` | Window baru |
| `w` | Daftar window |
| `0` / `1` / `2` | Loncat ke nomor window |
| `d` | Detach |

Hapus sesi: `tmux kill-session -t tantangan`.
