# GAME DESIGN DOCUMENT (GDD)

## 1. Thông tin chung

**Tên game:** Ball Blast
**Thể loại:** Arcade / Hyper-casual / Puzzle Action
**Nền tảng:** Mobile (Android / iOS)
**Engine:** Unity 6000
**Camera:** 2D – Orthographic
**Đối tượng người chơi:** Mọi lứa tuổi
**Phong cách:** Đơn giản – gây nghiện – phản xạ nhanh

---

## 2. Tổng quan gameplay

Ball Blast là game arcade bắn bóng số. Người chơi điều khiển một **pháo (cannon)** ở phía dưới màn hình, tự động bắn đạn để phá hủy các **quả bóng có số HP** rơi từ trên xuống.

* Mỗi quả bóng có số hiển thị = số lần cần bắn để phá hủy
* Khi bóng bị phá hủy có thể **tách thành các bóng nhỏ hơn**
* Người chơi cần **né bóng**, không để bóng chạm vào pháo

Game không có điểm kết thúc, mục tiêu là **sống càng lâu càng tốt** và đạt **score cao nhất**.

---

## 3. Cơ chế chơi chính

### 3.1 Điều khiển

* **Kéo trái / phải** để di chuyển pháo
* Pháo **tự động bắn liên tục** khi đang di chuyển
* Chỉ cần 1 tay để chơi

### 3.2 Pháo (Cannon)

* Vị trí cố định ở đáy màn hình
* Có thể nâng cấp:

  * Tốc độ bắn
  * Sát thương đạn
  * Tốc độ di chuyển

### 3.3 Bóng (Ball)

* Xuất hiện từ trên cao rơi xuống
* Có số HP hiển thị trực tiếp trên bóng
* Khi HP = 0:

  * Bóng nổ
  * Có thể chia thành 2 bóng nhỏ hơn

### 3.4 Va chạm & thua

* Nếu bất kỳ quả bóng nào chạm vào pháo → **GAME OVER**

---

## 4. Điều kiện thắng / thua

### Thắng

* Game **không có win cố định**
* Người chơi cố gắng sống lâu nhất có thể để đạt score cao

### Thua (Lose)

* Bóng chạm vào pháo

---

## 5. Cấu trúc Scene

### 5.1 Load Scene

* Logo game
* Thanh loading
* Khởi tạo:

  * Ads (AdMob)
  * Audio Manager
  * Save Data

### 5.2 Home Scene

* Button:

  * Play
  * Upgrade
  * Shop
  * Setting
* Hiển thị:

  * Coin hiện có
  * Best Score

### 5.3 Gameplay Scene

* Pháo ở đáy màn hình
* Bóng rơi từ trên
* UI:

  * Score hiện tại
  * Coin nhận được
  * Pause button

---

## 6. Hệ thống nâng cấp & Shop

### 6.1 Tiền tệ

* **Coin:** nhận khi phá hủy bóng

### 6.2 Nâng cấp pháo

* Fire Rate (tốc độ bắn)
* Damage (sát thương)
* Move Speed (tốc độ di chuyển)

### 6.3 Cosmetic (tuỳ chọn)

* Skin pháo
* Background

---

## 7. Hệ thống Popup

### 7.1 PopupPause

* Resume
* Restart
* Home

### 7.2 PopupLose

* Hiển thị score
* Button:

  * Revive (xem quảng cáo)
  * Retry
  * Home

### 7.3 PopupUpgrade

* Nâng cấp pháo bằng coin

### 7.4 PopupSetting

* Bật / tắt:

  * Nhạc nền
  * Âm thanh
  * Rung

---

## 8. Monetization

### 8.1 Quảng cáo (AdMob)

* **Rewarded Ads**:

  * Revive khi thua
  * X2 coin sau lượt chơi

* **Interstitial Ads**:

  * Sau X lượt chơi

### 8.2 In-App Purchase (IAP)

* Remove Ads
* Pack Coin

---

## 9. Âm thanh & hiệu ứng

### 9.1 Sound Effect (SFX)

* Bắn đạn
* Bóng nổ
* Thu coin
* UI click

### 9.2 Nhạc nền (BGM)

* Nhạc nhẹ, loop ngắn

---

## 10. Progression & Difficulty

* Thời gian chơi càng lâu:

  * Số lượng bóng tăng
  * HP bóng tăng
  * Tốc độ rơi nhanh hơn

* Có các mốc độ khó (wave)

---

## 11. Lưu trữ dữ liệu

* Save:

  * Best score
  * Coin
  * Upgrade level
  * Remove Ads

---

## 12. Mục tiêu thiết kế

* Hiểu luật chơi trong 2–3 giây
* Chơi nhanh, dễ gây nghiện
* Phù hợp thị trường hyper-casual / arcade
* Tối ưu quảng cáo và replay value

---

**End of GDD – Ball Blast**
