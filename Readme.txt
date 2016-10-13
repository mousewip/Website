Cấu hình kết nối database nằm trong:  src > conn > SQLServerConnUtils_SQLJDBC - sửa lại sqlInstanceName + password là được
SQLInstanceName là tên Server Name mà lúc login trên SQL server có thấy.

Đang gặp Bug khủng trong phần show sản phẩm, ae tìm cách fix hộ
(các thành phần liên quan đến bug: filter JDBCFilter, DBUtils, và jsp WEB-INF/views/productListView.jsp - hình như lỗi ở file này)

package:
	beans: mô phỏng bảng trong SQL
	conn: chịu trách nhiệm kết nối database
	filter: lọc các kết nối và truy vấn - chỉ cho những kết nối nào cần thiết dc phép đi qua
	servlet: ít nhất 1 servlet chịu trách nhiệm xử lí nhất 1 trang;
	utils: thao tác với database sau khi đã kết nối. VD: truy vấn query, thêm, sửa, xóa, update
các trang jsp: đọc tên cũng đủ biết