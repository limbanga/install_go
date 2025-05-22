## **Lesson 1: Install Go – Set Up Your Coding Path**

**Goal:** Install Go and set up your development environment so you can start coding right away.

---

### **Step 1: Download Go**

1. **Visit the official Golang website**:
   [https://go.dev/dl/](https://go.dev/dl/)

2. **Choose the version that matches your operating system**:

   * **Windows**: `.msi`
   * **macOS**: `.pkg`
   * **Linux**: `.tar.gz`

> Example: If you're using 64-bit Windows, download the `.msi` file.

---

### **Step 2: Install Go**

#### **Windows**

* Open the `.msi` file you downloaded.
* Follow the installation wizard.
* By default, Go will be installed at: `C:\Program Files\Go`

#### **macOS**

* Open the `.pkg` file and install it like a typical application.

#### **Linux**

Run the following commands (assuming you downloaded `go1.22.3.linux-amd64.tar.gz`):

```bash
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.22.3.linux-amd64.tar.gz
```

Then add this line to your `~/.bashrc` or `~/.zshrc` file:

```bash
export PATH=$PATH:/usr/local/go/bin
```

After that, run:

```bash
source ~/.bashrc  # or ~/.zshrc
```

---

### **Step 3: Check if Go is installed successfully**

Open Terminal (or Command Prompt) and type:

```bash
go version
```

> If you see something like `go version go1.22.3 linux/amd64`, the installation was successful!

---

### **Step 4: Set Up Your Workspace (GOPATH)**

* Create a working folder (e.g., `go-projects`)
* Add the following lines to your terminal config file:

```bash
export GOPATH=$HOME/go-projects
export PATH=$PATH:$GOPATH/bin
```

> Note: Since Go 1.11, you can use `go mod` for module management, so setting `GOPATH` is optional if you're using modules.

---

### **Step 5: Write Your First Program**

Create a file named `main.go` and add the following code:

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, Golang!")
}
```

Run the program:

```bash
go run main.go
```

> Output: `Hello, Golang!`

