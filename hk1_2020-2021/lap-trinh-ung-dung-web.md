## Native app - Hybrid app - Web app - Website
- **Native app:** là một ứng dụng gốc được thiết kế để hoạt động trên một nền tảng hay một thiết bị nhất định ( Android có JAVA, Kotlin,... ).
- **Hybrid app:** là một ứng dụng lai, là sự kết hợp giữa Native app và web app. Theo đó các phần cơ bản của ứng dụng được viết theo ngôn ngữ web nhưng được đặt trong native container. Vì là sự kết hợp điểm mạnh của native app và web app nên nó khai thác được trải nghiệm cao nhất của nền tảng.
- **Web app:**
  - Ứng dụng là một loại chương trình có khả năng làm cho máy tính thực hiện trực tiếp một công việc nào đó người dùng muốn thực hiện.
  - Web app là một ứng dụng web, chạy trên nền tảng web hoặc trình duyệt của các ứng dụng di động
- **Website:** còn gọi là trang web, là một tập hợp các trang web (webpage) và thường nằm trong cùng 1 tên miền hoặc tên miền phụ.
  - Webpage là 1 trang web tập hợp các đoạn văn bản, âm thành, video được tạo nên bởi HTML (ngôn ngữ đánh dấu văn bản).

## Quy trình phát triển phần mềm:
1. Lấy yêu cầu khách hàng và lên kế hoạch:
  - Tài liệu yêu cầu khách hàng
  - Tài liệu đề xuất giải pháp
  - Tài liệu quản lý dự án
2. Phân tích yêu cầu:
  - Tài liệu đặc tả yêu cầu phần mềm
3. Thiết kế:
  - Tài liệu thiết kế, mô hình, diagram, flowchart,...
  - Sơ đồ cấu trúc web, giao diện, kiến trúc ứng dụng, cơ sở dữ liệu, lưu đồ hoạt động, mô hình phân rã chức năng,...
4. Lập trình
5. Kiểm thử phần mềm
6. Cài đặt và bảo trì
  - Tài liệu hướng dẫn sử dụng, bảo trì.

## Một số thẻ HTML:
```
  a^2 -> A<sup>2</sup>
  A2 -> A<sub>2</sub>
```
Có thứ tự `ol`, không có thứ tự `ul`.

Thẻ `table`:
  - _cellpadding_: Khoảng cách 2 ô liên tiếp.
  - _cellspacing_: Padding trong ô.

## JQUERY
### Filter
| Filter    | Description                           |
|:----:     | :---                                  |
| :even     | Phần tử chẵn                          |
| :odd      | Phần tử lẽ                            |
| :eq(i)    | Phần tử tại vị trí i                  |
| :gt(i)    | Tất cả phần tử lớn hơn vị trí i       |
| :lt(i)    | Tất cả phần tử nhỏ hơn vị trí i       |
| :header   | Chọn tất cả các header (h1, ..., h6)  |
| :not(...) | Tất cả element không thỏa (...)       |

### Chèn nội dung
|         | Method      | Description                                    |
|:----:   |:----:       |:---                                            |
| $(e).   | append(c)   | Chèn nội dung _c_ vào cuối element thỏa **e**  |
|         | appendTo(c) | Chèn nội dung _e_ vào cuối element thỏa **c**  |
|         | after(c)    | Chèn nội dung _c_ vào sau element thỏa **e**   |
|         | before(c)   | Chèn nội dung _c_ vào trước element thỏa **e** |

Tương tự prepend(c).

## Cookie & Session
### Cookie
- Cookie là một đoạn văn bản ghi thông tin được tạo ra và lưu trên trình duyệt của máy người dùng. Cookie thường được tạo ra khi người dùng truy cập một website, cookie sẽ ghi nhớ những thông tin như tên đăng nhập, mật khẩu, các tuỳ chọn do người dùng lựa chọn đi kèm. Các thông tin này được lưu trong máy tính để nhận biết người dùng khi truy cập vào một trang web.
- Cookie thường được dùng để lưu trữ các tùy chọn riêng của trang web từng user, nó là một file nhỏ được Server chỉ định lưu trữ trên máy tính của Client và PHP có thể truy xuất tới được. Và để sử dụng được Cookie thì trình duyệt phải hỗ trợ chức năng này.
- Cookie sẽ không bị mất khi bạn đóng ứng dụng, nó phụ thuộc vào thời gian sống mà bạn thiết lập cho nó. Ví dụ bạn thiết lập Cookie lưu trữ thông tin đăng nhập trong vòng 15 phút thì sau 15 phút mà bạn không có một thao tác thay đổi trên nó thì Cookie của bạn sẽ bị chết.
### Session
- Session hay còn gọi là một phiên làm việc đơn giản là 1 cách để lưu lại dữ liệu của người dùng sử dụng website một cách tạm thời. Một session bắt đầu khi client gửi request đến sever, nó tồn tại xuyên suốt từ trang này đến trang khác trong ứng dụng và chỉ kết thúc khi hết thời gian timeout hoặc khi bạn đóng ứng dụng. Giá trị của session sẽ được lưu trong một tệp tin trên máy chủ.
- Bạn có thể tuỳ ý quyết định xem nên lưu trữ những thông tin nào vào Session, Thông thường chúng ta chỉ nên lưu trữ những thông tin tạm thời trong session.
- Với mỗi session sẽ được cấp phát một định danh duy nhất SessionID. Khi kết thúc một phiên làm việc và bắt đầu một phiên mới, dĩ nhiên sẽ được cấp một SessionID khác với trước đó.

## Procedure & Function in MySQL
### Procedure
- Procedure (Thủ tục) là một chương trình trong cơ sở dữ liệu gồm nhiều câu lệnh được lưu lại thành một nhóm đơn vị xử lý logic, được lưu trữ trên Database Server và được tái sử dụng cho những lần sau.
- Khi một câu lệnh gọi chạy stored procedure lần đầu tiên thì SQL Server sẽ chạy nó và lưu trữ vào **bộ nhớ đệm (plan cache)**, những lần tiếp theo SQL Server sẽ sử dụng lại plan cache nên sẽ cho tốc độ xử lý tối ưu.
- Stored procedure tiện lợi cho người quản trị database (DBA), giúp DBA tạo ra những nhóm câu lệnh và gửi đến một bô phận khác mà họ sẽ không cần quan tâm đến nội dung bên trong stored procedure có gì, mà chỉ quan tâm đến tham số đầu vào và đầu ra
Tính trừu tượng

**Ưu điểm:**
- **Tính trừu tượng:** Stored Procedure cung cấp một lớp trừu tượng cho các ứng dụng và ngôn ngữ
lập trình thao tác với hệ quản trị cơ sở dữ liệu. Việc thực hiện cùng 1 thao tác
giống nhau đến cơ sở dữ liệu trên 2 ứng dụng (hoặc nhiều hơn) hay ngôn ngữ lập
trình khác nhau không đòi hỏi người lập trình phải viết lại hoàn toàn các thao tác
đó.
- **Hiệu năng:** Stored Procedure được cung cấp bởi hệ quản trị cơ sở dữ liệu, được biên dịch và
lưu lại 1 lần duy nhất, được gọi đến và thao tác trực tiếp bởi hệ quản trị cơ sở dữ
liệu đó. Vì vậy, hiệu năng đạt được ở mức cao nhất mà hệ quản trị cơ sở dữ liệu
có thể thực hiện mà không phụ thuộc vào tính chất của ngôn ngữ lập trình bậc
cao nào.
- **Bảo mật:** Nếu hệ quản trị cơ sở dữ liệu được tùy chỉnh để chỉ có thể thực hiện thao tác gọi
đến các Stored Procedure có sẵn cho 1 số người dùng cụ thể, sẽ đảm bảo tính an
toàn của dữ liệu đối với những người dùng này. Việc phân quyền này đảm bảo
người dùng chỉ có quyền hạn thay đổi dữ liệu ở mức cho phép của người quản
trị cơ sở dữ liệu mà không thể can thiệp sâu hơn vào dữ liệu đó.

**Nhược điểm:**
- Nếu tạo ra quá nhiều Procedure thì hệ quản trị sẽ sử dụng bộ nhớ để lưu trữ các
thủ tục này khá nhiều. Ngoài ra nếu bạn thực hiện quá nhiều xử lý trong mỗi thủ
tục thì đồng nghĩa với việc CPU sẽ làm việc nặng hơn..
- Nếu sử dụng thủ tục thì sẽ rất khó phát triển trong ứng dụng, gây khó khăn ở
mức logic business.
- Một số hệ quản trị CSDL có những tool hỗ trợ Debug.
- Đòi hỏi kỹ thuật của người lập trình cơ sở dữ liệu tốt. Điều này làmcho vấn đề
bảo trì và nâng cấp khó khăn.