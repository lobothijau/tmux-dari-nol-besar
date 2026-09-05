# Solusi: tantangan-workflow

Pelajaran: [Tantangan: workflow pribadi](https://kodepas.com/kelas/tmux-dari-nol-besar/tantangan-workflow)

Ini contoh workflow, bukan satu-satunya cara yang "benar". Ganti nama sesi dan layout supaya cocok dengan kerjaanmu.

Lihat `WORKFLOW.md` untuk dua konteks (belajar vs kerja) dan `tmux.conf` untuk config yang selaras dengan cabang `final`.

## Ringkas

1. Dua sesi: `learn` (kelas Kodepas) dan `dev` (proyek)
2. `learn`: satu window `kelas`
3. `dev`: window `editor` + window `server` (dua pane: log + shell)
4. Config: salin `tmux.conf` ke `~/.tmux.conf`, reload
5. Selalu detach (`Ctrl+b d`); jangan `exit` kalau sesi masih dibutuhkan

```bash
cp tmux.conf ~/.tmux.conf
tmux source-file ~/.tmux.conf
```
