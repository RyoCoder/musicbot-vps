# Cara Deploy Bot Music Di Vps
Saya akan menjelaskan proses deploy bot music di vps secara detail, mohon disimak dengan seksama agar tidak keliru.

## Requirements
- Laptop, pc, atau lainnya.
- Tidak disarankan menggunakan hp karena akan ada file dengan ukuran besar yang harus diunduh.

## Awalan
- Silahkan membaca [laman ini](https://github.com/levina-lab/VPS_FREE/blob/4a8acd223e7379626f9471d756243e8e04b0c478/README.md) terlebih dahulu jika ingin menggunakan vps gratis.
- Disarankan untuk bertanya jika bingung, tanya ke [Grup Chat Telegram](https://t.me/gcsupportbots) saya jika ingin bertanya.
- Pada tutorial saat ini saya akan menggunakan repository dari [Geez Music Project](https://github.com/vckyou/Geez-MusicProject).

## Langkah-Langkah
- Buka terminal
- `git clone https://github.com/vckyou/Geez-MusicProject` untuk mengkloning repository.
- `cd Geez-MusicProject` untuk membuka directory file repo.
- `nvm install v15.1.0` untuk menginstall nodejs.
- `sudo apt-get install ffmpeg` jalankan ini setelah menginstall nodejs.
- `nano example env` buka file ini lalu isi vars nya, Jika sudah diisi, langsung Ctrl+X, lalu yes, lalu enter.
- `cd ..` lakukan ini sebanyak 4 kali sampai kembali ke awal dibagian Geez-MusicProject.
- `cd GeezProject` 
- `cd services` 
- `cd callsmusic` 
- `nano callsmusic.py` buka file ini, dibaris pytgcalls, clientid tambahkan koma (,) lalu masukkan angka yg sama sebanyak 4 digit.
- `cd ..` lakukan ini lagi sampai kembali ke awal.
- `pip3 install -r requirements.txt` untuk menginstall requirements text.
- `npm i -g npm` jalankan ini setelah menginstall requirements text.

## Jalankan Bot
- `cp example.env local.env` untuk menyalin vars dari example.env ke local.env
- `python3 -m GeezProject` untuk menjalankan bot, jika sudah aktif maka akan muncul tulisan "Started NodeJs Core", tandanya bot sudah aktif.
