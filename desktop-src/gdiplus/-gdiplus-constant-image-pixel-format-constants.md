---
description: Следующие константы, определенные в Гдиплуспикселформатс. h, указывают различные форматы пикселей, используемые в точечных рисунках.
ms.assetid: 362204c5-5dd7-461a-b90b-15826c025689
title: Константы формата пикселей изображения (Гдиплуспикселформатс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62abc8b0ed606b958764e27171f8b45e619d23b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987452"
---
# <a name="image-pixel-format-constants"></a>Константы формата пикселей изображения

Следующие константы, определенные в Гдиплуспикселформатс. h, указывают различные форматы пикселей, используемые в точечных рисунках.



| Константа                                                                                                                                                                                                                                     | Описание                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat1bppIndexed"></span><span id="pixelformat1bppindexed"></span><span id="PIXELFORMAT1BPPINDEXED"></span><dl> <dt>**PixelFormat1bppIndexed**</dt> </dl>             | Указывает, что формат имеет 1 бит на пиксель, индексированный.<br/>                                                                                                                                                         |
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>             | Указывает, что форматом отводится 4 бита на пиксель и цвета индексированы.<br/>                                                                                                                                                        |
| <span id="PixelFormat8bppIndexed"></span><span id="pixelformat8bppindexed"></span><span id="PIXELFORMAT8BPPINDEXED"></span><dl> <dt>**PixelFormat8bppIndexed**</dt> </dl>             | Указывает, что форматом отводится 8 бит на пиксель и цвета индексированы.<br/>                                                                                                                                                        |
| <span id="PixelFormat16bppARGB1555"></span><span id="pixelformat16bppargb1555"></span><span id="PIXELFORMAT16BPPARGB1555"></span><dl> <dt>**PixelFormat16bppARGB1555**</dt> </dl>     | Указывает, что формат имеет размер 16 бит на пиксель; 1 бит используется для альфа-компонента, а для красного, зеленого и синего компонентов используются 5 бит.<br/>                                                       |
| <span id="PixelFormat16bppGrayScale"></span><span id="pixelformat16bppgrayscale"></span><span id="PIXELFORMAT16BPPGRAYSCALE"></span><dl> <dt>**PixelFormat16bppGrayScale**</dt> </dl> | Указывает, что формат — 16 бит на пиксель, оттенки серого.<br/>                                                                                                                                                     |
| <span id="PixelFormat16bppRGB555"></span><span id="pixelformat16bpprgb555"></span><span id="PIXELFORMAT16BPPRGB555"></span><dl> <dt>**PixelFormat16bppRGB555**</dt> </dl>             | Указывает, что форматом отводится 16 бит на пиксель: по 5 бит на красный, зеленый и синий каналы. Оставшийся бит не используется.<br/>                                                                   |
| <span id="PixelFormat16bppRGB565"></span><span id="pixelformat16bpprgb565"></span><span id="PIXELFORMAT16BPPRGB565"></span><dl> <dt>**PixelFormat16bppRGB565**</dt> </dl>             | Указывает, что форматом отводится 16 бит на пиксель: по 5 бит на красный и синий канал, 6 бит на зеленый канал.<br/>                                    |
| <span id="PixelFormat24bppRGB"></span><span id="pixelformat24bpprgb"></span><span id="PIXELFORMAT24BPPRGB"></span><dl> <dt>**PixelFormat24bppRGB**</dt> </dl>                         | Указывает, что форматом отводится 24 бита на пиксель: по 8 бит на красный, зеленый и синий каналы.<br/>                                                                                                  |
| <span id="PixelFormat32bppARGB"></span><span id="pixelformat32bppargb"></span><span id="PIXELFORMAT32BPPARGB"></span><dl> <dt>**PixelFormat32bppARGB**</dt> </dl>                     | Указывает, что форматом отводится 32 бита на пиксель: по 8 бит на красный, зеленый и синий каналы, а также альфа-канал.<br/>                                                                                           |
| <span id="PixelFormat32bppPARGB"></span><span id="pixelformat32bpppargb"></span><span id="PIXELFORMAT32BPPPARGB"></span><dl> <dt>**PixelFormat32bppPARGB**</dt> </dl>                 | Указывает, что форматом отводится 32 бита на пиксель: по 8 бит на красный, зеленый и синий каналы, а также альфа-канал. Красный, зеленый и синий каналы умножаются в обратном порядке с учетом альфа-канала.<br/>   |
| <span id="PixelFormat32bppRGB"></span><span id="pixelformat32bpprgb"></span><span id="PIXELFORMAT32BPPRGB"></span><dl> <dt>**PixelFormat32bppRGB**</dt> </dl>                         | Указывает, что форматом отводится 32 бита на пиксель: по 8 бит на красный, зеленый и синий каналы. Оставшиеся 8 бит не используются.<br/>                                                               |
| <span id="PixelFormat48bppRGB"></span><span id="pixelformat48bpprgb"></span><span id="PIXELFORMAT48BPPRGB"></span><dl> <dt>**PixelFormat48bppRGB**</dt> </dl>                         | Указывает, что форматом отводится 48 бит на пиксель: по 16 бит на красный, зеленый и синий каналы.<br/>                                                                                                 |
| <span id="PixelFormat64bppARGB"></span><span id="pixelformat64bppargb"></span><span id="PIXELFORMAT64BPPARGB"></span><dl> <dt>**PixelFormat64bppARGB**</dt> </dl>                     | Указывает, что форматом отводится 64 бита на пиксель: по 16 бит на красный, зеленый и синий каналы, а также альфа-канал.<br/>                                                                                          |
| <span id="PixelFormat64bppPARGB"></span><span id="pixelformat64bpppargb"></span><span id="PIXELFORMAT64BPPPARGB"></span><dl> <dt>**PixelFormat64bppPARGB**</dt> </dl>                 | Указывает, что форматом отводится 64 бита на пиксель: по 16 бит на красный, зеленый и синий каналы, а также альфа-канал. Красный, зеленый и синий каналы умножаются в обратном порядке с учетом альфа-канала. <br/> |



## <a name="remarks"></a>Примечания

**PixelFormat48bppRGB**, **PixelFormat64bppARGB** и **PixelFormat64bppPARGB** используют 16 бит на каждый компонент цвета (канал). Windows GDI+ версии 1,0 может считывать изображения с 16 битами на канал, но такие образы преобразуются в формат 8 бит на канал для обработки, отображения и сохранения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Гдиплуспикселформатс. h</dt> </dl> |



 

 




