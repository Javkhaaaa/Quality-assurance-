Тайлан

- Хийсэн өөрчлөлтүүд:
  - JUnit 4-ийн нэгжийн тестүүд бичсэн: `CalendarTest`, `PersonTest`, `RoomTest`, `OrganizationTest`, `MeetingTest`.
  - Ant `build.xml` нэмсэн: `clean`, `compile`, `compile-tests`, `test`, `javadoc` target-ууд.
  - `README.md` шинэчилж, ажиллуулах заавар, тайланг нэмэв.

- Тестийн хамрах хүрээ ба тоо:
  - Нийт 21 тест:
    - `CalendarTest` – 9
    - `PersonTest` – 2
    - `RoomTest` – 2
    - `OrganizationTest` – 4
    - `MeetingTest` – 4

- Илрүүлсэн ба зассан алдаанууд:
  - `Calendar.checkTimes`: 12-р сарыг буруугаар хүчингүй гэж шалгаж байсан (>=12). 12-ыг зөвшөөрөхөөр (`>12`) засав.
  - `Calendar.isBusy` болон `Calendar.addMeeting`: Зөвхөн эхлэл/төгсгөлийн давхцлыг шалгадаг байсан тул "бүслэх" (enclosure) болон хүрэлцэх (touching) давхцлуудыг алгасдаг байсан. Одоо цагийн огтлолцол `start <= existingEnd && end >= existingStart` нөхцлөөр бүрэн шалгадаг болгосон.

- Ажиллуулах:
  - Нэгжийн тест: `ant test` (тайлан `build/reports`)
  - Javadoc: `ant javadoc` (гаралт `build/javadoc`)

- Санал болгох сайжруулалт:
  - Одон сар, өдрүүдийн хүчинтэй байдлыг бүрэн шалгах (сар бүрийн өдөр, өндрийн жил гэх мэт) — одоогоор "Day does not exist" хак ашигласан.
  - `Meeting` дээр `attendees` болон `room`-ийн null хамгаалалт нэмэх, builder эсвэл валидаци оруулах.
