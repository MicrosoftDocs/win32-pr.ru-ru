---
description: Запись звука
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Запись звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342015"
---
# <a name="audio-capture"></a>Запись звука

Приложение может использовать DirectShow для записи звуковых данных с микрофонов, проигрывателей лент и других устройств с помощью входов на звуковой карте. Типичные сценарии включают:

-   Запись речевого сопровождения VoiceOver для последующего дуббинг в потоке видео.
-   Преобразование устаревшего аналогового звукового содержимого в цифровой формат.
-   Запись голоса или музыки для передачи по сети.

У конечных пользователей есть несколько вариантов записи звука с звуковой платы на жесткий диск. Большинство карт предоставляют приложениям для смешивания звуковых входов и записи. Windows предоставляет средство записи звука, простое служебное приложение для записи с микрофона. Кодировщик Windows Media можно встроить в приложение DirectShow как [объект мультимедиа DirectX](directx-media-objects.md) (DMO). В этом разделе описывается интеграция функций аудиозаписи в свое приложение с помощью DirectShow.

В этом разделе рассматриваются следующие вопросы.

-   [О фильтре записи звука](about-the-audio-capture-filter.md)
-   [Выбор устройства записи](selecting-a-capture-device.md)
-   [Создание графика записи звука](creating-an-audio-capture-graph.md)
-   [Создание графика аудиозаписи с предварительной версией](creating-an-audio-capture-graph-with-preview.md)
-   [Настройка свойств записи звука](setting-audio-capture-properties.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование DirectShow](using-directshow.md)
</dt> </dl>

 

 



