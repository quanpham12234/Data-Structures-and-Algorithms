# Vector trong C++ (STL)

## 1. Khái quát về vector
- `vector` là một container thuộc **STL (Standard Template Library)**, hoạt động như một **mảng động**.
- Vector có thể **tự động thay đổi kích thước** khi thêm hoặc xóa phần tử.
- Có thể lưu trữ nhiều kiểu dữ liệu khác nhau: `int`, `string`, `pair`, `class`, `struct`, `vector`, `set`, ...
- Các phần tử trong vector được lưu trữ **liên tiếp trong bộ nhớ** và có thể truy cập thông qua chỉ số.

---

## 2. Vector Iterator
- Iterator là một đối tượng **hoạt động giống con trỏ**, dùng để trỏ tới các phần tử trong vector.
- Thông qua iterator, ta có thể truy cập và thay đổi giá trị phần tử.

Các iterator thường dùng:
- `begin()` : trỏ tới phần tử đầu tiên
- `end()` : trỏ tới vị trí **sau phần tử cuối**
- `rbegin()` : trỏ tới phần tử cuối (duyệt ngược)
- `rend()` : trỏ tới vị trí **trước phần tử đầu tiên**

---

## 3. Truy cập phần tử trong vector
- `front()` : trả về phần tử đầu tiên
- `back()` : trả về phần tử cuối cùng
- `operator[]` : truy cập phần tử theo chỉ số (không kiểm tra lỗi)
- `at()` : truy cập phần tử theo chỉ số (có kiểm tra phạm vi)

---

## 4. Duyệt vector
- Duyệt bằng chỉ số
- Duyệt bằng vòng lặp for-each (range-based for)
- Duyệt bằng iterator

---

## 5. Các hàm phổ biến trong vector
- `push_back(value)`  
  Thêm phần tử vào cuối vector.  
  Độ phức tạp: O(1) trung bình.

- `size()`  
  Trả về số lượng phần tử trong vector.

- `clear()`  
  Xóa toàn bộ phần tử trong vector.

- `empty()`  
  Trả về `true` nếu vector rỗng.

- `insert(iterator, value)`  
  Thêm phần tử tại vị trí xác định bằng iterator.  
  Độ phức tạp: O(N).

- `erase(iterator)`  
  Xóa phần tử tại vị trí xác định bằng iterator.  
  Độ phức tạp: O(N).

- `assign(n, value)`  
  Gán vector gồm `n` phần tử, tất cả đều bằng `value`.

- `resize(n)`  
  Thay đổi kích thước vector. Nếu tăng kích thước, các phần tử mới sẽ có giá trị mặc định.
