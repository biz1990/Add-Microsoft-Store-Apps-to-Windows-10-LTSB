# Add Microsoft Store Apps to Windows 10 LTSB without the Microsoft Store

To install the prerequisites for AppInstaller Right click on the "AppInstaller.ps1" PowerShell script, then click on "Run with PowerShell". 

To add store Apps you will need to download the required "appxbundle" file. 

For example to install "Photos" app you can either double click on the "appxbundle" file after installing the prerequisites, or run the command below in PowerShell replacing Microsoft.Windows.Photos.appxbundle with the correct file name. 

  - Add-AppxPackage -Path "*Microsoft.Windows.Photos.appxbundle"

Do Windows 10 LTSB bị lược bỏ hoàn toàn các gói hỗ trợ ứng dụng UWP, bạn cần chạy file cấu hình của liên kết này trước:Bạn tải toàn bộ mã nguồn từ link GitHub đó về máy tính (Nhấn nút Code màu xanh trên GitHub > Chọn Download ZIP, sau đó giải nén ra).Tìm đến file có tên là AppInstaller.ps1.Nhấp chuột phải vào file AppInstaller.ps1 và chọn Run with PowerShell.Đợi một lát để hệ thống cài đặt các gói hỗ trợ như VCLibs và AppInstaller hệ thống.
Bước 2: Tải file cài đặt ứng dụng Camera (.appxbundle)Trang GitHub bạn đưa chỉ hướng dẫn cách làm và cung cấp bộ cài nền tảng, họ không đính kèm sẵn file cài của ứng dụng Camera. 
Bạn cần tự tải file này từ nguồn chính thức của Microsoft:Truy cập vào trang web: https://rg-adguard.net (Đây là trang trung gian uy tín chuyên bóc tách link tải trực tiếp từ Microsoft Store).Dán link Microsoft Store của ứng dụng Camera này vào ô trống:texthttps://microsoft.com
Nhấn vào dấu Tích (v) bên cạnh để hệ thống quét link.Tìm và tải xuống file có đuôi .appxbundle hoặc .msixbundle có tên dạng: Microsoft.WindowsCamera_..._neutral_~_8wekyb3d8bbwe.appxbundle (Hãy chọn phiên bản có dung lượng nặng nhất, thường vài chục MB).
Bước 3: Tiến hành cài đặt Camera vào máy
Sau khi hoàn thành Bước 1, máy tính LTSB của bạn đã có khả năng đọc được định dạng file này. 
Bạn có 2 cách để cài:Cách đơn giản (Click đúp): Bạn chỉ cần nhấp đúp chuột trái vào file .appxbundle của Camera vừa tải về ở Bước 2. Một bảng thông báo hiện ra, bạn nhấn Install là xong.Cách dùng lệnh (Nếu click đúp bị lỗi):Nhấn giữ phím Shift + nhấp chuột phải vào một vùng trống trong thư mục chứa file Camera vừa tải > Chọn Open PowerShell window here.Copy và chạy lệnh sau (thay thế chính xác tên file bạn đã tải vào chỗ dấu ngoặc kép):powershellAdd-AppxPackage -Path "Tên_File_Camera_Của_Bạn.appxbundle"
Hãy thận trọng khi sử dụng mã.Sau khi chạy xong, bạn gõ tìm kiếm chữ Camera trong Menu Start, ứng dụng mặc định sẽ xuất hiện và hoạt động bình thường.
