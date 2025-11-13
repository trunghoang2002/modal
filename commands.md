---

## ⚙️ **1. Cấu hình & thiết lập ban đầu**

| Lệnh                | Mô tả                                                                                    |
| ------------------- | ---------------------------------------------------------------------------------------- |
| `modal setup`       | Thiết lập CLI lần đầu (login, cấu hình profile, token).                                  |
| `modal config`      | Quản lý cấu hình của client (xem, sửa, reset).                                           |
| `modal environment` | Tạo và quản lý **Environment** (tập hợp cấu hình runtime: secrets, queues, volumes,...). |
| `modal profile`     | Quản lý các **profile** (ví dụ: dev, prod).                                              |
| `modal token`       | Quản lý token đăng nhập (tạo mới, xoá, xác minh).                                        |

---

## 🚀 **2. Chạy & deploy ứng dụng**

| Lệnh                       | Mô tả                                                                            |
| -------------------------- | -------------------------------------------------------------------------------- |
| `modal run <script.py>`    | Chạy file Python có `@app.local_entrypoint()` hoặc `@app.function()` trên cloud. |
| `modal deploy <script.py>` | Deploy app Modal để gọi qua API, Dashboard, hoặc workflow khác.                  |
| `modal serve <script.py>`  | Chạy các endpoint web (FastAPI-like) và **hot reload code** khi đang dev.        |
| `modal launch`             | Mở một instance app serverless (tính năng experimental).                         |
| `modal shell`              | Mở **interactive shell** trong container của Modal (debug / test imports).       |

Sự khác biệt giữa 2 lệnh modal run và modal serve:
- modal run: Dùng để chạy một hàm hoặc file Python một lần rồi kết thúc
- modal serve: Dùng để deploy API/service chạy liên tục
---

## 🧩 **3. Quản lý ứng dụng**

| Lệnh                        | Mô tả                                                                |
| --------------------------- | -------------------------------------------------------------------- |
| `modal app list`            | Liệt kê các app đã deploy hoặc đang chạy.                            |
| `modal app show <app-name>` | Hiển thị thông tin chi tiết app (trạng thái, containers, functions). |
| `modal app logs <app-name>` | Xem log của app.                                                     |
| `modal app stop <app-name>` | Dừng app.                                                            |

---

## 🧱 **4. Quản lý container (thay cho image)**

| Lệnh                                            | Mô tả                                  |
| ----------------------------------------------- | -------------------------------------- |
| `modal container list`                          | Liệt kê các container đang chạy.       |
| `modal container logs <container-id>`           | Xem log realtime của container cụ thể. |
| `modal container exec <container-id> <command>` | Thực thi lệnh trong container.         |
| `modal container stop <container-id>`           | Dừng container đang chạy.              |

---

## 🧠 **5. Quản lý storage (Volume, Queue, Dict, Secret, NFS)**

| Lệnh                                         | Mô tả                                             |
| ---------------------------------------------| ------------------------------------------------- |
| `modal volume list`                          | Liệt kê tất cả volume trong Environment hiện tại. |
| `modal volume create <name>`                 | Tạo volume mới.                                   |
| `modal volume put <volume_name> <src> <dst>` | Upload file hoặc thư mục từ local lên volume.     |
| `modal volume get <path>`                    | Tải file xuống local.                             |
| `modal volume ls <path>`                     | Liệt kê file trong volume.                        |
| `modal volume rm <path>`                     | Xoá file hoặc thư mục trong volume.               |
| `modal volume cp <src> <dst>`                | Copy file trong cùng volume.                      |
| `modal volume delete <name>`                 | Xoá toàn bộ volume.                               |

Ngoài ra còn có:

* `modal queue` — quản lý hàng đợi công việc.
* `modal dict` — quản lý Dict (kv store).
* `modal secret` — tạo và quản lý secrets.
* `modal nfs` — làm việc với network filesystem (nếu app dùng nhiều node).

---

## 🧾 **6. Tiện ích & debug**

| Lệnh              | Mô tả                                 |
| ----------------- | ------------------------------------- |
| `modal --version` | Kiểm tra phiên bản CLI.               |
| `modal whoami`    | Hiển thị user/account đang đăng nhập. |
| `modal help`      | Hiển thị hướng dẫn tổng quan.         |

---