# Css
- reset trình duyệt
- căn chỉnh theo nội dung. vertical-align
# Tư duy khi làm
1. Nhìn website những thứ gì cố định thì tách ra 1 file css riêng, code html riêng. Mục đích để khi di chuyển sang file khác hoặc nếu khác hàng muốn chỉnh sửa giao diện thì chỉnh sửa 1 nốt nhạc.
# js
1. Dùng JS fetch include?
- file partials/header.html và partials/footer.html kết nối với index.html mục đích không muốn lặp lại giao diện footer và header
# Cấu trúc html
Product_chiThu
|-- backend
|-- frontend
    |-- assets
        |-- css
            |-- base
                |-- reset.css
            |-- components
                |-- header.css
                |-- footer.css
            |-- layout
                |-- container.css
                |-- grid.css
                |-- page.css
                |-- sidebar.css
        |-- js
            |-- component/
                |-- header.js
                |-- footer.js
                |-- modal.js
                |-- slider.js
            |-- utils/
                |-- animations.css
                |-- helpers.css
            |-- include.js
            |-- main.js
        |-- images
    |-- partials
        |-- header.html
        |-- footer.html
    |-- index.html
    |-- about.html
# Phát sinh lỗi khá hay
1. index.html:1 Refused to apply style from 'http://127.0.0.1:5500/frontend/assets/css/helper/flex.css' because its MIME type ('text/html') is not a supported stylesheet MIME type, and strict MIME checking is enabled.
2. cascade là gì.
3. Khi dùng flex thì phải chú ý tới chiều cao từng phần tử con.
    1. Nếu căn chỉnh khối thì lúc này phát sinh chiều cao không khớp với những khối còn lại => phát sinh ra lỗi.
    2. Cách chạy.
        flex-container
            |-- khối -> kế thừa từ html
                |-- con -> chỉ biết chạy theo chiều cao html
        flex-container
            |-- khối -> xét flex
                |-- con -> chiều cao con. Chiều cao con ảnh hưởng từ trong ra ngoài tất cả thẻ ngoại trừ thẻ xét height cứng