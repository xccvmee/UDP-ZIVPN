### MAKE ROOT ACCESS

<pre><code>wget -qO set-root "https://github.com/xccvmee/vip/releases/latest/download/set-root" && chmod +x set-root && sudo ALLOW_ROOT_PASSWORD=1 SET_ROOT_PASSWORD=1 ./set-root</code></pre>

### INSTALL SCRIPT
```bash
cat << 'EOF' > /usr/local/bin/sysctl
#!/bin/bash
# Jika ada perintah yang mencoba mengubah net.core (buffer jaringan), abaikan dan anggap sukses
if [[ "$*" == *"net.core."* ]]; then
    echo "[Bypass] Mengabaikan perintah sysctl pada container..."
    exit 0
fi
# Jika perintah sysctl lainnya, jalankan sysctl yang asli
exec /sbin/sysctl "$@"
EOF
```
```bash
chmod +x /usr/local/bin/sysctl
hash -r
```

<pre><code>apt update -y && apt install -y wget curl && wget -q https://raw.githubusercontent.com/xccvmee/udp-zivpn/main/setup.sh && chmod +x setup.sh && ./setup.sh
</code></pre>

<pre><code>wget -O /usr/local/bin/menu https://github.com/xccvmee/UDP-ZIVPN/releases/download/Latest/menu-amd64
</code></pre>

### UPDATE SCRIPT

<pre><code>wget -q https://raw.githubusercontent.com/xccvmee/udp-zivpn/main/update.sh && chmod +x update.sh && ./update.sh
</code></pre>

### PREVIEW SCRIPT

![IMAGE](https://raw.githubusercontent.com/xccvmee/udp-zivpn/main/SCRIPT.PNG)

## 📘 API Documentation

Lihat dokumentasi lengkap di sini 👉 [API Documentation](./zivpn_api.md)

### TESTED ON OS

- UBUNTU 24.10
- DEBIAN 12

### FITUR TAMBAHAN

- Pemasangan yang dinamis
- Notifikasi Backup To Email
- API Server
- Add Domain
- Auto delete expired
- Auto Backup
- Auto Clear LOG
- User Details Akun

### PORT INFO

```
- UDP-ZIVPN 1:65535
```

### SETTING CLOUDFLARE

```
- SSL/TLS : FULL
- SSL/TLS Recommender : OFF
```

### Auther

### CONTACT NEWBIE <br>

<a href="https://t.me/newbie_store24" target=”_blank”><img src="https://img.shields.io/static/v1?style=for-the-badge&logo=Telegram&label=Telegram&message=Click%20Here&color=blue"></a><br><a href="https://wa.me/6282326322300" target=”_blank”><img src="https://img.shields.io/static/v1?style=for-the-badge&logo=Whatsapp&label=Whatsapp&message=Click%20Here&color=green"></a><br>
