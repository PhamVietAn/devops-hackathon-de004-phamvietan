# DevOps Hackathon - Đe 004: Quan Ly kho hang (inventory)

## 1. Thong tin sinh vien

| Ho va ten | ma sinh vien | lop | tai khoan Linux | Github | cong Nginx |
| Pham Viet An | HN-PTIT-144 | KS24CNTT2 | crouan | PhamVietAn|  |

## 2. Moi truong trien khai
He dieu hanh: Ubuntu-24.04
phien ban Nginx:
Git:
noi chay: VPS

## 3. Cau truc du an

```
devops-hackathon-de004-phamvietan/
|-- src/                          # Web root (Nginx phục vụ thư mục này)
|   |-- index.html
|-- nginx/
|   |-- phamvietan-ks24cntt2.conf # Server block Nginx
|-- screenshots/                  # Ảnh minh chứng
|-- .gitignore
|-- README.md
```

## 4. Cau hinh Nginx

```bash
sudo cp /var/www/devops-hackathon-de004-phamvietan/nginx/phamvietan-ks24cntt2.conf \
  /etc/nginx/sites-available/phamvietan-ks24cntt2.conf
sudo ln -s /etc/nginx/sites-available/phamvietan-ks24cntt2.conf \
  /etc/nginx/sites-enabled/phamvietan-ks24cntt2.conf
sudo rm -f /etc/nginx/sites-enabled/default
sudo nginx -t
sudo systemctl reload nginx
```

## 5. Tuong lua UFW
```bash
sudo ufw allow 22/tcp
sudo ufw allow 8080/tcp
sudo ufw --force enable
sudo ufw status verbose
```
