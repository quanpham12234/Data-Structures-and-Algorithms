# Set trong C++ (STL)

## 1. Khái niệm
- `set` là một container trong thư viện **STL (Standard Template Library)** của ngôn ngữ lập trình C++.
- `set` là một container rất mạnh, giúp code trở nên **tối ưu và ngắn gọn** hơn trong nhiều bài toán.

---

## 2. Tính chất
- `set` là container mà **mỗi phần tử trong đó là duy nhất**, tức là không tồn tại hai phần tử có cùng giá trị.
- Các phần tử trong `set` được **tự động sắp xếp theo thứ tự tăng dần**:
  - Tăng dần theo giá trị đối với kiểu số
  - Tăng dần theo thứ tự từ điển đối với kiểu chuỗi ký tự

---

## 3. Cú pháp
```cpp
set<data_type> set_name;
set<int> s;
set<string> st;

```
## 4. Sử dụng set
- Phù hợp với các bài toán mà thao tác thêm, xóa, tìm kiếm phần tử được thực hiện nhiều lần.
- Thường dùng trong các bài toán liên quan đến các giá trị khác nhau của mảng (loại bỏ phần tử trùng lặp).

## 5. Một số hàm trong set

- `insert(value)`  
  Thêm một phần tử vào set.  
  Độ phức tạp: `O(logN)`.

- `size()`  
  Trả về số lượng phần tử trong set.

- `empty()`  
  Kiểm tra set có rỗng hay không.  
  Nếu rỗng trả về `true`, ngược lại trả về `false`.

- `clear()`  
  Xóa toàn bộ phần tử trong set.

- `find(value)`  
  Kiểm tra sự tồn tại của một phần tử trong set.  
  - Trả về iterator tới phần tử nếu tìm thấy  
  - Trả về `end()` nếu phần tử không tồn tại trong set  
  Độ phức tạp: `O(logN)`.

- `count(value)`  
  Dùng để đếm số lần xuất hiện của một phần tử trong set.  
  (Trong set, giá trị trả về chỉ có thể là `0` hoặc `1`)  
  Độ phức tạp: `O(logN)`.

- `erase(value)`  
  Xóa một phần tử khỏi set nếu phần tử đó tồn tại.  
  Nếu phần tử không tồn tại, hàm **không gây lỗi runtime**.  
  Độ phức tạp: `O(logN)`.
