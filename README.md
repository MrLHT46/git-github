# git-github
## Stash All Changes là một chức năng cực kỳ hữu ích trong Git, đặc biệt khi bạn đang code dở mà cần chuyển nhánh / kéo code / sửa nóng 👇

#🧠 Hiểu nhanh trong 1 câu

Stash All Changes = cất toàn bộ code đang sửa vào “ngăn tủ tạm” để quay về trạng thái sạch như chưa sửa gì

📌 Không mất code
📌 Không cần commit
📌 Có thể lấy lại sau

## 🗂 Trạng thái trước & sau khi stash
# 🔴 Trước

File modified

File staged

File chưa add

Code đang dang dở

# 🟢 Sau stash

Working tree sạch

Giống như vừa checkout từ commit mới nhất

# 🔧 Thực chất Git làm gì?
git stash


Git sẽ:

Lưu toàn bộ thay đổi (cả staged + unstaged)

Đưa thư mục về trạng thái clean

## 🖱 Trong VS Code
✅ CÁCH TỐT NHẤT: STASH (có đặt tên) ⭐⭐⭐
🔹 Lưu lại mốc an toàn
git stash push -m "SAFE POINT: map render ok"
📌 Cách này:

Không commit

Không ảnh hưởng history

Quay lại được bất cứ lúc nào
 hoặc click “Stash All Changes” hay:
Stash All Changes ≈
git stash push

## 🔄 Lấy code ra lại (rất quan trọng)
# ✅ Lấy và xóa khỏi stash
git stash pop

# ✅ Lấy nhưng giữ lại trong stash
git stash apply

# 📦 Nhiều stash thì sao?
git stash list


Ví dụ:

stash@{0}: WIP on main: map feature
stash@{1}: WIP on dev: fix bug


# Áp dụng stash cụ thể:

git stash apply stash@{1}

# ⚠️ Phân biệt với commit
Stash	Commit
Tạm thời	Lưu lâu dài
Không message bắt buộc	Có message
Không xuất hiện trong history	Có
Dùng khi code dở	Dùng khi code ổn
# 🚀 Khi nào nên dùng Stash?

✔ Đang code dở
✔ Cần git pull mà Git không cho
✔ Muốn chuyển branch nhanh
✔ Tránh commit rác

# 🧠 Câu nhớ nhanh

Stash = Ctrl + Z cho cả project (nhưng an toàn hơn)
==================================================
##
