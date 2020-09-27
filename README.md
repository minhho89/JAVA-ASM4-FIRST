# JAVA-ASM4-FIRST
Hướng dẫn dự án
 Bookmark this page
Hướng dẫn dự án

Mô tả ứng dụng

Ứng dụng cần phải đảm bảo các chức năng cơ bản. Tuy nhiên, bạn có thể thêm chức năng bổ sung vào ứng dụng của bạn, nếu bạn muốn.

Phần 1: Chức năng và yêu cầu cơ bản

1. Thiết kế giao diện

Giao diện đơn thuần dạng console
Hiển thị thông tin thành khối rõ ràng và dễ nhìn
2. Yêu cầu chức năng cơ bản

1. Hiển thị danh sách nhân viên hiện có trong công ty

2. Hiển thị các bộ phận trong công ty

3. Hiển thị các nhân viên theo từng bộ phận

4. Thêm nhân viên mới vào công ty: bao gồm 2 loại

- Thêm nhân viên thông thường 

- Thêm nhân viên là cấp quản lý (có thêm chức vụ)

5. Tìm kiếm thông tin nhân viên theo tên hoặc mã nhân viên
6. Hiển thị bảng lương của nhân viên toàn công ty
7. Hiển thị bảng lương của nhân viên theo thứ tự tăng dần

Phần 2. Tổ chức code

File Employee.java là định nghĩa cho class nhân viên
File Manager.java là định nghĩa cho class quản lý
File Department.java là định nghĩa cho class bộ phận
File HumanResources.java là class chứa luồng chính của chương trình
Phần 3. Tài nguyên

Không có tài nguyên ban đầu.

Phần 4. Hướng dẫn chi tiết

Trước khi bắt đầu làm project thì hãy đọc bài viết này để hiểu rõ về cách làm
Tham khảo thêm bài viết về cách sử dụng ArrayList https://www.javatpoint.com/java-arraylist

Tạo project Human Resources
Tạo file Staff.java là class abstract chứa các thông tin cơ bản của nhân viên, hàm toString() là hàm abstract, các class kế thừa triển khai hiển thị thông tin phù hơp
Thuộc tính: mã nhân viên, tên nhân viên, tuổi nhân viên, hệ số lương, ngày vào làm, bộ phận làm việc, số ngày nghỉ phép

4. Tạo file Employee.java: chứa thông tin chung về nhân viên, bao gồm các thuộc tính và phương thức sau.

 - Thuộc tính: số giờ làm thêm

 - Phương thức: calculateSalary() trả về lương nhân viên, toString() hiển thị thông tin nhân viên.

- Employee kế thừa class Staff

5. Tạo interface ICalculator chứa hàm tính lương, các class nhân viên và quản lý implement interface để tính lương phù hợp

6. Tạo file Department.java: chứa thông tin chung về bộ phận, bao gồm các thuộc tính và phương thức sau.

 - Thuộc tính: mã bộ phận, tên bộ phận, số lượng nhân viên hiện tại

 - Phương thức: toString() hiển thị thông tin về bộ phận. 

7. Tạo file Manager.java: chứa thông tin chung về quản lý, bao gồm các thuộc tính và phương thức sau. 

 - Thuộc tính: chức danh

 -  Phương thức: toString() hiển thị thông tin bao gồm cả chức danh

 -  Thừa kế: Manager cũng là nhân viên, nên sẽ thừa kế từ class Staff. 

9. Tạo file HummanResources.java: chứa thông tin chung về nhân viên, bao gồm các thuộc tính và phương thức sau.

 - Tạo ra hàm main để xử lý luồng chính của chương trình 

 - Dùng vòng lặp do…while để cho phép người dùng chọn lại chức năng 

 - Triển khai các chương trình theo yêu cầu

Công thức tính lương:

Nhân viên: Hệ số lương * 3,000,000 + số giờ làm thêm * 200,000

Quản lý: Hệ số lương * 5,000,000 + lương trách nhiệm

Lương trách nhiệm:

Business Leader = 8,000,000

Project Leader = 5,000,000

Technical Leader = 6,000,000
