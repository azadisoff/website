# Git Code

*** khởi tạo Git trên thư mục đã chọn ***

git init //create Git local repository


*** cấu hình lần đầu tiên cho Local repository ***    

git config --global user.name "w3schools-test"
git config --global user.email "test@w3schools.com"

*** liệt kê danh sách các tiệp trong thư mục ***

ls //danh sách các tập tin và thư mục

*** tạo một thư mục mới cho dự án của chúng ta ***    

mkdir [name] //tạo thư mục mới
rmdir [name] //xoá thư mục
cd [name]    //chuyển đến thư mục làm việc

*** tạo & xóa một tập tin mới  ***    

touch [name] //tạo một tập tin mới
rm [filename] //xóa tập tin như ở hệ điều hành
git rm --cached [filename] // xóa khỏi vùng Staged
git rm -f [filename] // xóa tập tin trong vùng Staged
git restore --staged [filename] // phục hồi tập tin vùng Staged
git restore [filename] // phục hồi tập tin đã delete

*** đổi tên một tập tin mới  ***    

git mv [filename] [filename] // đổi tên tập tin 

*** kiểm tra trạng thái Git ***

git status
git status --short //xem trạng thái ngắn gọn của file

Note:   ?? - Tệp không theo dõi
        A - Các tệp được thêm vào vùng hiển thị
        M - Các tệp đã sửa đổi
        D - Các tệp đã xóa

*** thêm file vào Staged ***

git add [file]
git add * //thêm tất cả các file

*** chuyển từ staged sang commit cho repository ***

git commit -m "comment"
git commit -a -m "comment" //bỏ qua bước git add [file]

*** xem lịch sử các cam kết cho một kho lưu trữ ***

git log
git log --oneline

*** phân nhánh trong Git ***

git branch [name]   //create một phân nhánh
git branch -d [name]   //delete một phân nhánh
git branch          //xem nhánh đang làm việc
git checkout [name] //chuyển sang nhánh mới
git checkout -b [name] //create và chuyển sang nhánh mới

*** hợp nhất các phân nhánh vào nhánh chính ***

git checkout master // chọn nhánh chính
git merge branch    // hợp nhất với phân nhánh

*** Git ignore ***

touch .gitignore //khởi tạo tập tin .gitignore

*** Remote Repository ***

git remote add origin [URL] //thêm tên của Remote
git remote rm remote-name //xóa một địa chỉ remote
git remote -v //xem thông tin các Remote có trong Local
git remote show origin //xem thông tin chi tiết về một Remote
git remote rename origin azadi //đổi tên một Remote trong Local
git fetch origin //kiểm tra dữ liệu mới từ Remote Repository
git pull origin main //Lấy toàn bộ dữ liệu mới theo Remote
git push origin main //cập nhật dữ liệu từ Local lên Remote
git push origin main --force //ghi đè toàn bộ dữ liệu từ Local lên remote
