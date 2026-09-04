100 DAYS VTUBER MEMORIAL — V2 SYSTEM EDITION

Mở index.html.

V2 thay đổi:
- Thêm âm thanh procedural bằng Web Audio API, không cần tải file âm thanh ngoài.
- Boot sound khi người xem tương tác lần đầu.
- Typing/log beeps cho từng dòng hệ thống.
- Success chime khi DAY 100 ACHIEVED.
- Low system hum trong archive.
- Click sound khi chuyển màn hình.
- Phần Memory Archive và Final Letter đã đổi hoàn toàn sang phong cách terminal/system,
  thống nhất với opening.
- Không cần internet, framework hay thư viện ngoài.

Nội dung cần thay:
- [VTuber's Name]
- [Tên của bạn]
- Các memory/video
- Nội dung letter.

Lưu ý: trình duyệt chặn autoplay, vì vậy âm thanh được kích hoạt từ lần click/tap đầu tiên.


AUDIO INTEGRATION
-----------------
The uploaded computer-noise.mp3 is included at:
  sounds/computer-noise.mp3

It is used as a low-volume looping computer-processing ambience during the
system boot sequence. It fades out when the DAY 100 ACHIEVED state is reached.

Browser autoplay policy means the sound begins after the visitor's first
click/tap/key interaction. The visual boot sequence itself is unchanged.


AUTOPLAY / REPLAY
-----------------
The computer-noise.mp3 now attempts to start automatically when the page loads,
without requiring a first click. It loops during the system-processing intro
and fades out at DAY 100 ACHIEVED.

Important: browsers such as Chrome/Edge can block unmuted audio autoplay based
on their autoplay policy. The website therefore attempts autoplay first and
uses the first user interaction only as a fallback if the browser blocks it.

When the intro/reboot flow is run again, the same audio is restarted from the
beginning.


AUDIO BEHAVIOR
--------------
computer-noise.mp3 is now restricted to the opening System Boot sequence.

- Starts automatically when the page loads (subject to browser autoplay policy).
- Loops only while the opening boot sequence is running.
- Stops and resets when DAY 100 ACHIEVED. appears.
- Does NOT restart when entering Memory Archive or Final Message.
- There is intentionally no reboot/click handler that restarts the audio.


FINAL MESSAGE SCROLL FIX
------------------------
- The Final Message section can now expand vertically with the full letter.
- Vertical page scrolling is enabled.
- Letter content is no longer clipped by fixed-height containers.
- Replay/Reboot controls are forced back into normal document flow.
- Extra bottom spacing is added so the replay control stays inside the visible page.
