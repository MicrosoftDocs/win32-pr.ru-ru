---
description: Форматы пикселей с высоким динамическим диапазоном
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Форматы пикселей с высоким динамическим диапазоном
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911940"
---
# <a name="high-dynamic-range-pixel-formats"></a>Форматы пикселей с высоким динамическим диапазоном

Кодеки должны использовать форматы пикселей компонента Windows Imaging Component (WIC), сохраняющие весь динамический диапазон базовых данных датчика. GUID \_ WICPixelFormat48bppRGB — это типичный формат 16-разрядного канала с фиксированной точкой, который можно использовать. Также можно использовать и другие форматы с более высокой точностью. Чтобы обеспечить полную поддержку конвейера отрисовки графического процессора (GPU) Windows Presentation Foundation, корпорация Майкрософт настоятельно рекомендует поддержку 32-разрядного формата пикселей с плавающей точкой.

Форматы пикселей с высоким цветом. в Windows 7 добавлены два новых формата пикселей WIC для поддержки новых форматов дисплеев высокого цвета. Это: GUID \_ WICPixelFormat32bppRGBA1010102 и GUID \_ WICPixelFormat32bppRGBA1010102XR.

Формат высокого цвета с 16 битами на канал (бит/с) поддерживается существующим \_ форматом GUID WICPixelFormat64bppRGBAHalf пикселей.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Рекомендации по WIC для форматов необработанных изображений Camera](-wic-rawguidelines.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



