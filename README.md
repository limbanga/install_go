## **Lesson 1: Install Go – Set Up Your Coding Path**

**Mục tiêu:** Cài đặt Go và thiết lập môi trường phát triển để bạn có thể bắt đầu lập trình ngay.

---

### **Bước 1: Tải Go**

1. **Truy cập trang chính thức của Golang**:
   [https://go.dev/dl/](https://go.dev/dl/)

2. **Chọn phiên bản phù hợp với hệ điều hành của bạn**:

   * **Windows**: `.msi`
   * **macOS**: `.pkg`
   * **Linux**: `.tar.gz`

> Ví dụ: Nếu bạn dùng Windows 64-bit, hãy tải file `.msi`.

---

### **Bước 2: Cài đặt Go**

#### **Windows**

* Mở file `.msi` vừa tải.
* Làm theo hướng dẫn để cài đặt.
* Mặc định, Go sẽ được cài vào: `C:\Program Files\Go`

#### **macOS**

* Mở file `.pkg` và cài đặt như ứng dụng thông thường.

#### **Linux**

Chạy lệnh sau (giả sử bạn tải về file `go1.22.3.linux-amd64.tar.gz`):

```bash
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.22.3.linux-amd64.tar.gz
```

Thêm dòng sau vào file `~/.bashrc` hoặc `~/.zshrc`:

```bash
export PATH=$PATH:/usr/local/go/bin
```

Sau đó chạy:

```bash
source ~/.bashrc  # hoặc ~/.zshrc
```

---

### **Bước 3: Kiểm tra Go đã cài thành công chưa**

Mở Terminal (hoặc CMD) và gõ:

```bash
go version
```

> Nếu bạn thấy kết quả như: `go version go1.22.3 linux/amd64` thì bạn đã cài đặt thành công!

---

### **Bước 4: Thiết lập thư mục làm việc (GOPATH)**

* Tạo thư mục làm việc (ví dụ: `go-projects`)
* Thêm vào file cấu hình terminal:

```bash
export GOPATH=$HOME/go-projects
export PATH=$PATH:$GOPATH/bin
```

> Ghi chú: Từ Go 1.11 trở lên, bạn có thể dùng `go mod` và không cần cấu hình `GOPATH` nữa, nên bước này có thể bỏ qua nếu bạn dùng `go mod`.

---

### **Bước 5: Viết chương trình đầu tiên**

Tạo file `main.go` với nội dung:

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, Golang!")
}
```

Chạy chương trình:

```bash
go run main.go
```

> Kết quả: `Hello, Golang!`
