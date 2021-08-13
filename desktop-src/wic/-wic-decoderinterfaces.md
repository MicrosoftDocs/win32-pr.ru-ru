---
description: Интерфейсы декодера
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Интерфейсы декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a52a0924f6302e45b10cb32a1d621db04967d33a3251ee39cce359e5030af5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393532"
---
# <a name="decoder-interfaces"></a>Интерфейсы декодера

в следующих таблицах показаны интерфейсы, реализованные с помощью декодеров Windows imaging Component (WIC), а на схеме классов показана иерархия наследования.

Интерфейсы декодера Container-Level



| Интерфейс                                                                                       | Обязанности                             | Реализация                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [ивикбитмапдекодер](-wic-imp-iwicbitmapdecoder.md)                                             | Службы уровня контейнера                     | Обязательно                                                                   |
| [ивикбитмапкодекпрогресснотификатион](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Уведомление о ходе выполнения & поддержка отмены | Рекомендуется                                                                |
| [ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md)                                 | Перечисление метаданных                         | Необязательный (требуется только для форматов, поддерживающих метаданные уровня контейнера) |



 

Интерфейсы декодера Frame-Level



| Интерфейс                                                           | Обязанности          | Реализация                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Службы уровня кадров      | Обязательно                      |
| [ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md)     | Перечисление метаданных      | Обязательно                      |
| [ивикбитмапсаурцетрансформ](-wic-imp-iwicbitmapsourcetransform.md) | Встроенные преобразования декодера | Рекомендуется                   |
| [ивикдевелоправ](-wic-imp-iwicdevelopraw.md)                       | Службы обработки RAW   | Требуется только для необработанных форматов |



 

![Иерархия наследования интерфейса WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Реализация декодера WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Реализация Ивикбитмапдекодер](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



