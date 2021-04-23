---
description: Следующие подтипы определяют несжатые форматы RGB без альфа-канала.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Несжатые подтипы видео RGB (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894034c01b42f58cbc6a1e5a5c7fe6d77f50befd
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909532"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Несжатые подтипы видео RGB

Следующие подтипы определяют несжатые форматы RGB без альфа-канала.



| Константа                                                                                                                                                                        | Описание                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ RGB1**</dt> </dl>       | RGB, 1 бит на пиксель (бит/с), палеттизед<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ RGB4**</dt> </dl>       | RGB, 4 бит, палеттизед<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ RGB8**</dt> </dl>       | RGB, 8 бит, палеттизед<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ RGB555**</dt> </dl> | RGB 555, 16 бит/пкс<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ RGB565**</dt> </dl> | RGB 565, 16 бит/пкс<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ Rgb24**</dt> </dl>    | RGB, 24 бит/с<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ RGB32**</dt> </dl>    | RGB, 32 бит/с<br/>                            |



Следующие подтипы определяют форматы несжатых RGB с альфа-каналом.



| Константа                                                                                                                                                                                       | Описание                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ ARGB1555**</dt> </dl>          | RGB 555 с альфа-каналом<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ ARGB32**</dt> </dl>                | RGB 32 с альфа-каналом<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ ARGB4444**</dt> </dl>          | 16-разрядный RGB с альфа-каналом; 4 бита на канал<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ A2R10G10B10**</dt> </dl> | 32-разрядный RGB с альфа-каналом; 10 бит на канал RGB плюс 2 бита для альфа.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**МЕДИАСУБТИПЕ \_ A2B10G10R10**</dt> </dl> | 32-разрядный BGR с каналом альфа; 10 бит на канал BGR плюс 2 бита для Alpha.<br/> |



## <a name="remarks"></a>Комментарии

Для форматов палеттизед цвет каждого пикселя задается в виде индекса в палитре. Палитра должна быть включена в блок формата после структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Для форматов, отличных от палеттизед, цвет каждого пиксела указывается напрямую; Макет памяти зависит от глубины бита:

-   В RGB 555 используется следующий макет памяти:
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   В RGB 565 используется следующий макет памяти:
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   Для RGB 24 каждый пиксель является [**ргбтрипле**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple). Каждый цвет имеет один байт со значением от 0 до 255 включительно. Макет памяти: 

| Метка | Значение |
    |-------|------|-------|-----|
    | Byte  | 0    | 1     | 2   |
    | Значение | Синий | Зеленый | Красный |

    

     

-   Для RGB 32 каждый пиксель является **ргбкуад**. Каждый цвет имеет один байт со значением от 0 до 255 включительно. Макет памяти: 

| Метка | Значение |
    |-------|------|-------|-----|---------------------|
    | Byte  | 0    | 1     | 2   | 3                   |
    | Значение | Синий | Зеленый | Красный | Альфа или не нужно |

    

     

    If the subtype is MEDIASUBTYPE\_ARGB32, byte 3 contains a value for the alpha channel. If the subtype is MEDIASUBTYPE\_RGB32, byte 3 should be ignored.

-   A2R10G10B10 использует следующий макет: 

| Метка | Значение |
    |-------|-------|---------|---------|---------|
    | bit   | 0–9 | 10–19 | 20 - 29 | 30 - 31 |
    | Значение | Синий  | Зеленый   | Красный     | Коэффициент альфа   |

    

     

-   A2B10G10R10 использует следующий макет: 

| Метка | Значение |
    |-------|-------|---------|---------|---------|
    | bit   | 0–9 | 10–19 | 20 - 29 | 30 - 31 |
    | Значение | Красный   | Зеленый   | Синий    | Коэффициент альфа   |

    

     

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Подтипы видео](video-subtypes.md)
</dt> <dt>

[Работа с кадрами видео](working-with-video-frames.md)
</dt> </dl>

 

 
