# Camera

Samsung Galaxy A17 (Android 15) uchun oddiy va tezkor kamera ilova. Kotlin + CameraX.

## Imkoniyatlar
- **FOTO**: yuqori sifatli JPEG (4:3), Pictures/Camera papkasiga saqlanadi
- **HARAKAT**: Motion Photo (surat + ~1.7 soniyalik video, Google formati)
- **VIDEO**: 9:16, FHD gacha, ovoz bilan (ruxsat berilsa)
- Bosib fokus, ikki barmoq bilan zoom, chaqmoq (o'chiq/avto/yoniq, videoda fonar)
- Taymer (3s / 10s), uchdan bir to'ri, old/orqa kamera
- Ovoz tugmalari shutter vazifasini bajaradi
- Qurilma burilishiga qarab to'g'ri yo'nalishda saqlash

## Ochish
1. Android Studio (Ladybug yoki yangiroq) → **Open** → `Camera` papkasi
2. Gradle sync tugashini kuting (internet kerak)
3. Telefonda USB debugging yoqing va **Run**

> `gradle-wrapper.jar` arxivga kirmagan. Android Studio uni avtomatik yuklaydi.

## Motion Photo (pre-roll bilan)
Kamera kadrlari doimiy ravishda xotiradagi aylanma buferga yig'iladi (oxirgi 1 soniya).
Tugma bosilganda **oldingi 1 soniya + keyingi 0.8 soniya** H.264 (MP4) ga kodlanadi
va suratning JPEG fayli ichiga Google Motion Photo formatida joylanadi.

- Klip ovozsiz, 960x720 atrofida
- Old kamerada klip va surat ikkalasi ham ko'zguda aks ettirilmaydi
- Kodlash kechiksa (6 soniyadan ko'p), surat oddiy JPEG sifatida saqlanadi

## Saqlash joyi
Surat va videolar `DCIM/Camera` papkasiga saqlanadi (Samsung Gallery'dagi "Camera" albomi),
shuning uchun darhol galereyada ko'rinadi.
