# SECURE CODING HANDBOOK

## Phân quyền

| Role | Truy cập repo | Chỉnh sửa repo | Tạo issue | Tạo pull request | Duyệt pull request | Cấu hình repo |
| --- | --- | --- | --- | --- | --- | --- |
| Admin | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |  :heavy_check_mark: |
| Contributer | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |  |
| User | :heavy_check_mark: |  | :heavy_check_mark: | :heavy_check_mark: |  |  |

- [Hướng dẫn sử dụng](#truy-cập-handbook)
- [Quy trình contribute](#quy-trình-contribute)

## Truy cập handbook

1. Người dùng thường truy cập vào handbook, lựa chọn nền tảng code muốn xem trong nhánh **main**
    ![alt text](asset/image.png)
1. Lựa chọn ngôn ngữ và framework muốn xem
    ![alt text](asset/image_1.png)
2. Sau khi chọn ngôn ngữ, trang web hiển thị danh sách các lỗ hổng theo từng chức năng. Người dùng bấm vào lỗ hổng trong chức năng cần xem
    ![alt text](asset/image_2.png)
3. Nội dung bao gồm các ví dụ về uncompliance code và gợi ý compliance code
    ![alt text](asset/image_3.png)

## Tạo issue

Người dùng có thể tạo issue refer trực tiếp tới vị trí bị lỗi

![alt text](asset/image_4.png)

Mô tả vấn đề cần được giải quyết

![alt text](asset/image_5.png)

Ngoài ra, có thể refer issue tới các issue khác, commit, pull request

## Tạo pull request

Người dùng thường fork repo và chỉnh sửa trên bản fork đó. 

![alt text](asset/image_6.png)

Trong trường hợp người dùng muốn tạo 1 file lỗ hổng mới thì phải sử dụng [template vuln](Templates/Web/vuln.md) và cập nhật tên lỗ hổng vào file **readme** của folder đó. Tên file lỗ hổng không viết hoa để đồng nhất với repo.

Sau khi chỉnh sửa, commit change và tạo pull request tới repo chính

![alt text](asset/image_7.png)

![alt text](asset/image_8.png)

Chọn draft a pull request để contributer theo dõi và duyệt request

![alt text](asset/image_9.png)

**Lưu ý trước khi thực hiện pull request, người dùng phải đảm bảo update repo tới phiên bản mới nhất để tránh xảy ra conflict khi merge request**

## Quy trình contribute

Admin hoặc Contributer kiểm tra pull request và assign 1 người khác để review pull request

![alt text](asset/image_11.png)

Người được assign review pull request và đánh dấu đã review

![alt text](asset/image_10.png)

**Nếu xuất hiện conflict ở bước này, yêu cầu người dùng update repo và tạo lại pull request.** 

Contributer thực hiện merge request sau các bước kiểm tra

![alt text](asset/image_12.png)

