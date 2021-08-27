---
description: Запись звука
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Запись звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f76924e170c29e4488e2b7bd31bddbe8702ebe78d9ed146471bdfa21598d12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108714"
---
# <a name="audio-capture"></a>Запись звука

приложение может использовать DirectShow для записи звуковых данных с микротелефонов, проигрывателей лент и других устройств с помощью входов на звуковой карте. Распространенные сценарии

-   Запись речевого сопровождения VoiceOver для последующего дуббинг в потоке видео.
-   Преобразование устаревшего аналогового звукового содержимого в цифровой формат.
-   Запись голоса или музыки для передачи по сети.

У конечных пользователей есть несколько вариантов записи звука с звуковой платы на жесткий диск. Большинство карт предоставляют приложениям для смешивания звуковых входов и записи. Windows предоставляет средство записи звука, простое служебное приложение для записи с микрофона. кодировщик Windows Media можно включить в DirectShowное приложение как [объект мультимедиа DirectX](directx-media-objects.md) (DMO). В этом разделе описано, как интегрировать функции записи звука в свое приложение с помощью DirectShow.

В этом разделе рассматриваются следующие вопросы.

-   [О фильтре записи звука](about-the-audio-capture-filter.md)
-   [Выбор устройства записи](selecting-a-capture-device.md)
-   [Создание Graph записи звука](creating-an-audio-capture-graph.md)
-   [создание записи аудио Graph с предварительной версией](creating-an-audio-capture-graph-with-preview.md)
-   [Настройка свойств записи звука](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование DirectShow](using-directshow.md)
</dt> </dl>

 

 



