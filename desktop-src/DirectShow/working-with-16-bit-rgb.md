---
description: Работа с 16-разрядным RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Работа с 16-разрядным RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683627"
---
# <a name="working-with-16-bit-rgb"></a>Работа с 16-разрядным RGB

Для 16-битного RGB определены два формата:

-   МЕДИАСУБТИПЕ \_ 555 использует по пять бит для красного, зеленого и синего компонентов в пикселях. Наиболее важный бит в **слове** игнорируется.
-   МЕДИАСУБТИПЕ \_ 565 использует пять бит для красного и синего компонентов и шесть бит для зеленого компонента. Этот формат отражает тот факт, что человеческие концепции наиболее чувствительны к зеленым частям видимого спектра.

**RGB 565**

Чтобы извлечь цветовые компоненты из изображения RGB 565, рассматривайте каждый пиксель как тип **слова** и используйте следующие битовые маски:


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Получите цветовые компоненты из пикселя следующим образом:


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



Помните, что красный и синий каналы имеют 5 бит, а зеленый канал — 6 бит. Чтобы преобразовать эти значения в 8-разрядные компоненты (для 24-разрядного или 32-разрядного RGB), необходимо сдвинуть соответствующее число битов влево:


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Отмените этот процесс, чтобы создать RGB 565 пикселей. Предполагая, что значения цвета были усечены до правильного числа битов:


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

Работа с RGB 555, по сути, аналогична RGB 565, за исключением того, что битовые маски и операции сдвига в битах различаются. Чтобы получить цветовые компоненты с пикселя RGB 555, выполните следующие действия.


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



Чтобы упаковать значения красного, зеленого и синего цветов в RGB 555 пикселей, выполните следующие действия.


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Несжатые подтипы видео RGB](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



