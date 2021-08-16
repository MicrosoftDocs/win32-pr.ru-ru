---
description: Форматы пикселей с высоким динамическим диапазоном
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Форматы пикселей с высоким динамическим диапазоном
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086917"
---
# <a name="high-dynamic-range-pixel-formats"></a>Форматы пикселей с высоким динамическим диапазоном

в кодеки должны использоваться форматы пикселей Windows изображений (WIC), сохраняющие весь динамический диапазон базовых данных датчика. GUID \_ WICPixelFormat48bppRGB — это типичный формат 16-разрядного канала с фиксированной точкой, который можно использовать. Также можно использовать и другие форматы с более высокой точностью. чтобы обеспечить полную поддержку конвейера отрисовки графического процессора (GPU) Windows Presentation Foundation, корпорация майкрософт настоятельно рекомендует поддержку 32-разрядного формата пикселей с плавающей точкой.

форматы пикселей с высоким цветом. в Windows 7 добавлены два новых формата пикселей WIC для поддержки новых форматов дисплеев высокого цвета. Это: GUID \_ WICPixelFormat32bppRGBA1010102 и GUID \_ WICPixelFormat32bppRGBA1010102XR.

Формат высокого цвета с 16 битами на канал (бит/с) поддерживается существующим \_ форматом GUID WICPixelFormat64bppRGBAHalf пикселей.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Рекомендации по WIC для форматов необработанных изображений Camera](-wic-rawguidelines.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



