# Hướng dẫn đóng gói
***Lưu ý: Chỉ sử dụng với mục đích deploy không sử dụng với mục đích develop***

***Sử dụng CLI***.
***Công cụ cần thiết: git cli, docker cli***

Mở terminal (Linux) hoặc command promp (linux)

**1. Clone repo trên github về máy**
```
git clone https://github.com/quangtho908/cnpm-website.git
```

**2. Sau khi clone trên thư mục hiện hành sẽ xuất hiện một hư mục có tên**
cnpm-website truy cập vào thư mục này
```
cd cnpm-website
```

**3. Sử dụng docker để tạo 1 image với tag là cnpm-website.**
Linux: \
```
sudo docker build -t cnpm-website .
```
Windows: 
```
docker build -t cnpm-website .
```

**4. Chờ đến khi docker build thành công chúng ta sẽ có một image kiểm tra**
image này đã tồn tại hay chưa bằng lệnh sau:
Linux: 
```
sudo docker image ls
```
Windows:
```
docker image ls
```
Kết quả như sau
```
REPOSITORY TAG IMAGE ID CREATED SIZE
cnpm latest dc2db531fbd1 39 minutes ago 780MB
Image đã được tạo thành công
```
**5. Run image này với port 8080.**
Linux: 
```
sudo docker run -p 8080:8080 cnpm
```
Windows: 
```
docker run -p 8080:8080 cnpm
```

**6. mở `https://localhost:8080` và xem kết quả**
