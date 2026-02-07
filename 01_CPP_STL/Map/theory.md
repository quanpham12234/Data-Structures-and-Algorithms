# MAP, MULTIMAP, UNORDERED_MAP

---

## 1. MAP

### 1.1 Khái niệm

`map` là một container giúp lưu các phần tử theo cặp **key - value** (khóa - giá trị).  
Mỗi key ánh xạ tới một value tương ứng.  

So với `set`, `map` mạnh mẽ hơn và giải quyết được nhiều bài toán thực tế hơn.

---

### 1.2 Tính chất

- Các **key là duy nhất**, không có hai key nào trùng nhau  
- **Value có thể trùng**
- Các phần tử được **sắp xếp tăng dần theo key**
- Mỗi phần tử là một `pair`:
  - `first` : key
  - `second`: value

---

### 1.3 Cú pháp

```cpp
map<key_data_type, value_data_type> map_name;

```
---

### 1.4 Khi nào dùng map?
- Các bài toán liên quan tới tần suất xuất hiện
- Các bài toán cần thêm / xóa / tìm kiếm nhanh
- Thay cho mảng đánh dấu khi dữ liệu lớn hoặc không liên tục

---

### 1.5 Một số hàm quan trọng trong map

- **insert(key, value)**  
  Thêm một cặp (key, value) vào map.  
  Nếu key đã tồn tại thì cặp mới sẽ không được thêm.  
  Độ phức tạp: `O(logN)`.

- **operator[] (map[key])**  
  Dùng để truy cập hoặc gán value cho một key.  
  Nếu key chưa tồn tại, map sẽ tự động tạo phần tử mới.  
  Độ phức tạp: `O(logN)`.

- **size()**  
  Trả về số lượng cặp phần tử trong map.

- **empty()**  
  Kiểm tra map có rỗng hay không.  
  Trả về `true` nếu rỗng, ngược lại trả về `false`.

- **clear()**  
  Xóa toàn bộ phần tử trong map.

- **find(key)**  
  Tìm kiếm một key trong map.  
  Trả về iterator tới phần tử nếu tìm thấy, ngược lại trả về `end()`.  
  Độ phức tạp: `O(logN)`.

- **count(key)**  
  Kiểm tra sự tồn tại của key trong map.  
  Vì key là duy nhất nên hàm chỉ trả về `0` hoặc `1`.  
  Độ phức tạp: `O(logN)`.

- **erase(key / iterator)**  
  Xóa phần tử khỏi map thông qua key hoặc iterator.  
  Độ phức tạp: `O(logN)`.

---

## 2. MULTIMAP

### 2.1 Khái niệm

`multimap` tương tự như `map`, nhưng cho phép **nhiều key có cùng giá trị** tồn tại trong container.

---

### 2.2 Tính chất

- Các key **không bắt buộc duy nhất**
- Các phần tử vẫn được **sắp xếp tăng dần theo key**
- Mỗi phần tử là một cặp `key - value`
- **Không hỗ trợ** truy cập value thông qua cú pháp `mp[key]`

---

### 2.3 Khi nào dùng multimap?

- Khi cần lưu **nhiều giá trị cho cùng một key**
- Các bài toán nhóm dữ liệu theo key
- Các bài toán cần giữ **thứ tự tăng dần của key**

---

### 2.4 Một số hàm khác biệt trong multimap

- **find(key)**  
  Trả về iterator tới **phần tử đầu tiên** có key tương ứng.

- **count(key)**  
  Trả về số lần xuất hiện thực tế của key trong multimap.

- **erase(key)**  
  Xóa **tất cả** các phần tử có key tương ứng.

- **erase(iterator)**  
  Chỉ xóa phần tử mà iterator đang trỏ tới.

---

## 3. UNORDERED_MAP

### 3.1 Khái niệm

`unordered_map` là một container lưu trữ các cặp **key - value** tương tự `map`,  
nhưng **không duy trì thứ tự sắp xếp của key**.

---

### 3.2 Tính chất

- Các key là **duy nhất**
- Các phần tử **không được sắp xếp**
- Dựa trên **hash table** để lưu trữ dữ liệu

---

### 3.3 Độ phức tạp

- Trong trường hợp trung bình:
  - `insert`, `find`, `erase`: `O(1)`
- Trong trường hợp xấu nhất:
  - Độ phức tạp có thể lên tới `O(N)`

---

### 3.4 Khi nào dùng unordered_map?

- Khi **không cần thứ tự**
- Khi ưu tiên **tốc độ truy cập**
- Các bài toán xử lý dữ liệu lớn, cần tối ưu thời gian

---

## 4. So sánh nhanh

| Container        | Key trùng | Sắp xếp | Độ phức tạp |
|------------------|-----------|----------|--------------|
| map              | ❌        | ✅       | `O(logN)`    |
| multimap         | ✅        | ✅       | `O(logN)`    |
| unordered_map    | ❌        | ❌       | `O(1)` TB    |


