# Giới thiệu

**Space Hunter** là một tựa game bắn súng sinh tồn (Arcade Shooter) được phát triển bằng Unity Engine. Trong game, người chơi sẽ điều khiển một chiến binh không gian tiêu diệt kẻ thù và thu thập các vật phẩm nâng cấp để sinh tồn lâu nhất có thể. Game nổi bật với hệ thống nâng cấp sức mạnh mang phong cách roguelike và độ khó tự động tăng tiến theo thời gian.

---

## Cách chơi

- Sử dụng phím **Mũi tên Lên/Xuống** (Up/Down Arrow) để di chuyển.
- Nhấn phím **Space** để bắn đạn.
- Chú ý lượng đạn hiển thị trên màn hình. Súng sẽ cần thời gian để nạp lại đạn (Reload) tự động.
- Nhặt các vật phẩm (Boost) để nhận ngẫu nhiên các loại nâng cấp (Tăng lượng đạn tối đa, Giảm thời gian nạp đạn, Tăng sát thương).

---

## Tính năng nổi bật & Kỹ thuật lập trình

- **Tối ưu hóa hiệu suất (Object Pooling):** Toàn bộ đạn (Bullets) và vật phẩm (Boosts) sinh ra trong game đều được tái sử dụng qua một hệ thống `ObjectPooler`.
- **Kiến trúc Generic Singleton:** Triển khai một class `Singleton<T>` độc lập để quản lý dễ dàng, an toàn các hệ thống cốt lõi (Managers) như `GameManager`, `EnemyManager`, `BoostManager`, `SFXManager`,... tránh lặp lại code.
- **Hệ thống Nâng cấp (Weighted Random Gacha):** Tính năng lõi của game. Khi nhặt vật phẩm, game sẽ chọn ngẫu nhiên ra 3 thẻ nâng cấp. Tỉ lệ rớt của mỗi thẻ không bằng nhau mà được tính toán dựa trên thuật toán Trọng số (Weighted Random), giúp cân bằng game.
- **Độ khó tăng tiến (Dynamic Difficulty):** Sử dụng các `Coroutine` để liên tục buff thêm máu tối đa và tốc độ di chuyển cho kẻ thù sau mỗi khoảng thời gian người chơi sinh tồn, tạo ra nhịp độ game càng lúc càng dồn dập.

---

## Công nghệ sử dụng

- **Engine:** Unity
- **Ngôn ngữ:** C#
- **Design Patterns:** Object Pooling, Singleton Pattern.

---

## Hướng dẫn cài đặt

- Tải game trên itch.io: https://buingocbuu.itch.io/space-hunter
- Giải nén file **Space-Hunter.rar**
- Chạy file **Space Hunter.exe**
