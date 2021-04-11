---
title: Интерполяция кадров
description: Интерполяция кадров
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK, интерполяция кадров
- кодеки, интерполяция кадров
- Интерполяция кадров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069570"
---
# <a name="frame-interpolation"></a>Интерполяция кадров

Интерполяция кадров — это процесс создания промежуточных видеокадров на основе данных в двух последовательных кадрах закодированного видео. Фактически интерполяция кадров увеличивает [*частоту кадров*](wmformat-glossary.md) закодированного видео во время декодирования. Интерполяцию кадров можно использовать для повышения гладкости воспроизведения видеопотоков с низкой частотой кадров.

Поскольку это функция декодирования, она не включает специальные параметры кодирования и не требует дополнительной нагрузки на содержимое. Интерполяция кадров указывается в качестве выходного параметра в объекте Reader.

Только кодек Windows Media Video 9 поддерживает интерполяцию кадров.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Функции кодеков**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2:: Сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Параметры вывода**](output-settings.md)
</dt> </dl>

 

 




