# Arch Linux-ni o'rnatish bo'yicha bosqichma-bosqich qo'llanma

## I. Kirish

Arch Linux nima ekanligini qisqacha tushuntirish: Arch Linux Linux yadrosiga asoslangan bepul va Open Source operatsion tizimdir. Bu doimiy ravishda yangilanadigan distributivdir, ya'ni u doimiy ravishda yangilanadi va foydalanuvchilar eng so'nggi dasturiy ta'minot yangilanishlari va xavfsizlik tuzatishlarini oladi. Arch Linux o'zining soddaligi, moslashuvchanligi va minimalizmi bilan mashhur va o'z tizimini to'liq nazorat qilishni xohlaydigan tajribali Linux foydalanuvchilariga mo'ljallangan.

Qo'llanmaning maqsadi: Ushbu qo'llanmaning maqsadi Arch Linuxni o'rnatish bo'yicha to'liq va bosqichma-bosqich qo'llanmani taqdim etishdir. Ushbu qo'llanma Arch Linux-ga yangi kelgan va uni sinab ko'rmoqchi bo'lgan yangi boshlanuvchilarga, shuningdek Arch Linux-ni o'z tizimlariga o'rnatmoqchi bo'lgan tajribali Linux foydalanuvchilariga yordam berish uchun mo'ljallangan.

Qo'llanma uchun maqsadli auditoriya: Ushbu qo'llanmaning maqsadli auditoriyasi tajriba darajasidan qatiy nazar, Arch Linuxni qanday o'rnatishni o'rganishga qiziqqan har bir kishidir. Qo'llanma Arch Linuxni o'z tizimlariga o'rnatishning oddiy va tushunarli usulini izlayotgan yangi boshlanuvchilar va tajribali Linux foydalanuvchilari uchun javob beradi.

## II. Tizim talablari

Minimal qurilma talablari: Arch Linux-ni muvaffaqiyatli o'rnatish uchun tizimingiz quyidagi minimal qurilma talablariga javob berishi kerak:

* 64 bitli protsessor
* Kamida 512 MB operativ xotira
* Kamida 200 MB bo'sh joyga ega yuklanadigan xotira qurilmasi

Tavsiya etilgan apparat spetsifikatsiyalari: Arch Linux bilan eng yaxshi tajribaga ega boʻlish uchun quyidagi texnik xususiyatlarga ega boʻlish tavsiya etiladi:

* Kamida 2 yadroli zamonaviy 64 bitli protsessor
* Kamida 2 GB operativ xotira
* Kamida 20 Gb bo'sh joyga ega hard disk yoki ssd disk.

Mavjud xotira maydoni: Arch Linux uchun zarur bo'lgan xotira maydoni tizimdan maqsadli foydalanishga va o'rnatiladigan dasturiy ta'minotga bog'liq. Umumiy qoida sifatida, asosiy o'rnatish uchun kamida 20 GB bo'sh joy bo'lishi tavsiya etiladi. Agar siz qo'shimcha dasturlarni o'rnatishni yoki katta hajmdagi fayllarni saqlashni rejalashtirmoqchi bo'lsangiz, sizga ko'proq xotira kerak bo'lishi mumkin.

## III. O'rnatishga tayyorlanish

Arch Linux ISO-ni USB diskiga yozish: Arch Linux-ni o'rnatishdan oldin, Arch Linux ISO bilan yuklanadigan USB diskini yaratishingiz kerak. Buning uchun siz Rufus yoki Etcher kabi vositalardan foydalanishingiz mumkin va yoki linux terminali orqali xam yozishingiz mumkin. Arch Linux ISO-ning so'nggi versiyasini rasmiy Arch Linux veb-saytidan yuklab oling va keyin ISO-ni USB diskiga yozish uchun ushbu vositadan foydalaning.

#### [Arch Linuxni yuklab olish](http://mirror.yandex.ru/archlinux/iso/2023.02.01/)

Havola orqali `.iso` foramatini yuklab oling (tepadan 3 chi)

Arch linuxni linux terminali orqali USB ga yozish

```bash
dd bs=4M if=/home/ismoilovdev/Documents/archlinux-x86_64.iso of=/dev/sdb conv=fsync oflag=direct status=progress
```
bu yerda siz ISO faylga yo'l berasiz masalan `/home/ismoilovdev/Document/archlinux-x86_64.iso`

`of=/dev/sdb` bu yerda mening USB draverim formati sizda boshqacha bo'lishi mumkin buni bilish uchun terminalga root bilan kirib quyidagi buyruqni kiriting> USB drayver kompyuterga ulangan bo'lishi kerak.
```bash
sudo su 
fdisk -l
```
Chiqqan ma'lumotlardan eng pastida USB drayver haqida yozilgan bo'ladi turlari `/dev/sda, /dev/sdb, /dev/sdx` 

USB orqali yuklash: yuklanadigan USB drayverini yaratganingizdan so'ng, kompyuteringizni USB bilan yuklashingiz kerak. Buni amalga oshirish uchun USB drayverini kompyuteringizga joylashtiring va uni qayta ishga tushiring. Kompyuteringizning BIOS yoki UEFI konfiguratsiyasiga qarab, yuklash menyusiga kirish va yuklash qurilmasi sifatida USB drayverini tanlash uchun tugmani (masalan, F12 yoki Esc) bosishingiz kerak bo'ladi.

![alt text](https://www.wimware.com/design/how-to/boot-from-cd-dvd/Boot-options-entry-key.png)

Rasmda keng tarqalgan kompyuter brednlarining boot menuga kirish usullari

Boot menuga kiring va USB ni tanlab enter bosing

Internetga ulanish: Sozlaganingizga qarab, Arch Linux o'rnatilishini yakunlash uchun internetga ulanishingiz kerak bo'ladi. O'rnatish jarayonida yangilanishlar yoki paketlarni yuklab olishingiz kerak bo'lsa, bu ayniqsa muhimdir. Internetga ulanish uchun simli internet yoki simli internet bo'lmasa USB kabel bilan telefondan USB Modemni yoqish va yoki  Wi-Fi tarmog'iga ulashingiz mumkin.