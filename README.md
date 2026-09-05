# tmux dari Nol — starter

Titik awal kelas [tmux dari Nol](https://kodepas.com/kelas/tmux-dari-nol-besar).

File `.tmux.conf` di sini adalah pratinjau Modul 7: mouse, history panjang, dan copy-mode vi. Tantangan konfigurasi menambah satu key binding kustom. Cabang `final` adalah hasil lengkap Modul 7–8.

## Prasyarat

- Terminal (macOS, Linux, atau WSL)
- tmux terpasang — `tmux -V`

## Pasang

```bash
git clone https://github.com/kodepas/tmux-dari-nol-besar.git
cd tmux-dari-nol-besar
git checkout starter
cp .tmux.conf ~/.tmux.conf
tmux source-file ~/.tmux.conf
```

Kalau belum ada sesi tmux, `tmux new` dulu baru `source-file`.

## Lanjut

- Tantangan: lihat folder di cabang `main`
- Hasil akhir: `git checkout final`
