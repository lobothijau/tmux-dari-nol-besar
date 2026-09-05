# tmux dari Nol — repo latihan

Materi pendamping kelas [tmux dari Nol](https://kodepas.com/kelas/tmux-dari-nol-besar) di Kodepas.

Repo ini berisi file konfigurasi tmux dan solusi tiap **Tantangan**. Video dan catatan lengkap ada di situs; di sini kamu mengetik perintah di terminal sendiri.

## Prasyarat

- Laptop atau komputer dengan terminal (macOS, Linux, atau WSL di Windows)
- Sudah pernah membuka terminal dan mengetik satu perintah (misalnya `ls`)
- tmux terpasang (`tmux -V` menampilkan versi). Kalau belum, ikuti [Modul Instalasi](https://kodepas.com/kelas/tmux-dari-nol-besar/install-tmux)

Tidak perlu akun GitHub untuk mengikuti kelas. GitHub hanya untuk mengunduh file ini.

## Clone

```bash
git clone https://github.com/kodepas/tmux-dari-nol-besar.git
cd tmux-dari-nol-besar
```

## Cabang

| Cabang | Isi |
|---|---|
| `starter` | `.tmux.conf` minimal + langkah pasang |
| `final` | Konfigurasi lengkap Modul 7–8 (mouse, history, key binding) |
| `main` | Solusi 8 Tantangan (satu folder per pelajaran) |

Mulai dari starter:

```bash
git checkout starter
cp .tmux.conf ~/.tmux.conf
tmux source-file ~/.tmux.conf
```

Lihat hasil akhir Modul 7–8:

```bash
git checkout final
```

## Solusi Tantangan

Coba dulu tanpa membuka folder solusi. Setiap folder memakai slug pelajaran di Kodepas:

| Folder | Pelajaran |
|---|---|
| [`tantangan-perkenalan/`](./tantangan-perkenalan) | Sesi tmux pertama |
| [`tantangan-instalasi/`](./tantangan-instalasi) | Pasang tmux di mesin sendiri |
| [`tantangan-sesi-window/`](./tantangan-sesi-window) | Layout 3 window |
| [`tantangan-pane/`](./tantangan-pane) | Layout coding dua pane |
| [`tantangan-detach/`](./tantangan-detach) | Sesi yang selamat dari disconnect |
| [`tantangan-copy/`](./tantangan-copy) | Salin error dari log |
| [`tantangan-konfigurasi/`](./tantangan-konfigurasi) | tmux.conf starter |
| [`tantangan-workflow/`](./tantangan-workflow) | Workflow pribadi |

## Lisensi

MIT. Silakan pakai dan ubah konfigurasinya untuk workflow-mu sendiri.
