---
description: Функции видео и изображений
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Функции видео и изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab4b57f804c1da1e4a6da0ca4625e3503ed9987077a80f1f98dde91cf2e27f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432124"
---
# <a name="video-and-image-functions"></a>Функции видео и изображений

эти функции и макросы управляют структурой формата видео DirectShow.



| Функция                                                             | Описание                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_совпадение битовых масок \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Сравнивает цветовые маски для двух структур [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                                       |
| [**БИТОВОЙ маски**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Извлекает цветовые маски из структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**чекквидеоинфотипе**](checkvideoinfotype.md)                     | Проверяет тип носителя, содержащий структуру формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , для ошибок, которые могут привести к переполнениям буфера или переполнению целочисленных значений.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Проверяет тип носителя, содержащий структуру формата [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , для ошибок, которые могут привести к переполнениям буфера или переполнению целочисленных значений. |
| [**КРАСОК**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Получает записи палитры из структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**контаинспалетте**](containspalette.md)                           | Определяет, содержит ли указанная структура [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) палитру.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Преобразует тип мультимедиа, использующий [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , в объект, использующий [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**дибсизе**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Вычисляет число байтов, необходимых для аппаратно-независимого точечного рисунка (DIB).                                                                                     |
| [**жетбиткаунт**](getbitcount.md)                                   | Возвращает число битов на пиксель, используемое указанным подтипом видео.                                                                                           |
| [**жетбитмапформатсизе**](getbitmapformatsize.md)                   | Вычисляет размер, необходимый для структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , которая может содержать указанную структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .       |
| [**жетбитмаппалетте**](getbitmappalette.md)                         | Возвращает первую запись палитры в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                        |
| [**жетбитмапсизе**](getbitmapsize.md)                               | Вычисляет число байтов, необходимых для аппаратно-независимого точечного рисунка (DIB).                                                                                     |
| [**жетбитмапсубтипе**](getbitmapsubtype.md)                         | Возвращает **GUID** подтипа носителя для указанного точечного рисунка.                                                                                                      |
| [**жетсубтипенаме**](getsubtypename.md)                             | Извлекает удобное для восприятия имя подтипа видео.                                                                                                             |
| [**жеттруеколортипе**](gettruecolortype.md)                         | Возвращает **GUID** подтипа носителя для 16-разрядного растрового изображения RGB.                                                                                          |
| [**ЗАГОЛОВОК**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Возвращает адрес [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader).                                      |
| [**\_ \_ Сведения о последовательности MPEG1**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Возвращает адрес заголовка последовательности в структуре [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .                                                          |
| [**палеттисед**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Проверяет, имеет ли точечный рисунок глубину цвета 8 бит или меньше.                                                                                                      |
| [**записи ПАЛИТРы \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Возвращает максимальное число цветов в палитре указанного точечного рисунка.                                                                                      |
| [**СБРОСИТЬ \_ маски**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Заполняет поля цветовой маски в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) нулями.                                                                            |
| [**СБРОСИТЬ \_ заголовок**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Заполняет [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) нулями.                                                                                                   |
| [**СБРОСИТЬ \_ палитру**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Заполняет записи палитры в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) нулями.                                                                              |
| [**\_ \_ Палитра размера Ега**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Вычисляет размер, необходимый для записей палитры в 4-битовом битовом изображении RGB.                                                                                         |
| [**\_маски размера**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Вычисляет размер цветовых масок в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                             |
| [**РАЗМЕР \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Вычисляет размер структуры [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) , включая заголовок последовательности.                                                      |
| [**\_Палитра размера**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | Вычисляет размер записей палитры в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                         |
| [**\_заголовок размера**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Вычисляет смещение в байтах для поля **бмихеадер** в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                              |
| [**РАЗМЕР \_ видеохеадер**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Вычисляет размер структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                                  |
| [**труеколор**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Возвращает структуру [**труеколоринфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) из структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                            |
| [**валидатебитмапинфохеадер**](validatebitmapinfoheader.md)         | Проверяет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) на наличие ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.                                   |



 

## <a name="remarks"></a>Remarks

Большинство макросов и функций, описанных в разделе, предназначены для управления структурами **видеоинфохеадер** и **видеоинфо** для растровых изображений RGB. Используйте эти макросы с осторожностью. в большинстве случаев предполагается, что указанная структура инициализирована правильно. Многие из них также предполагают, что структура **битмапинфохеадер** является стандартным размером. то есть `biSize == sizeof(BITMAPINFOHEADER)` .

DirectShow библиотека базовых классов также предоставляет следующие глобальные константы, которые определяют стандартные цветовые маски для одноцветных точечных рисунков.



| Глобальные данные | Описание                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Массив цветовых масок для 16-битного растрового изображения RGB в формате 5-5-5. |
| **bits565** | Массив цветовых масок для 16-битного растрового изображения RGB в формате 5-6-5. |
| **bits888** | Массив цветовых масок для 24-битового растрового изображения RGB.                 |



 

Каждая из этих констант в массиве из трех **DWORD**, содержащая красные, зеленые и синие маски в этом порядке.

 

 
