---
description: Преобразователь tee/Sink-to-Sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Преобразователь tee/Sink-to-Sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674163"
---
# <a name="teesink-to-sink-converter"></a>Преобразователь tee/Sink-to-Sink

Преобразователь tee/Sink-to-Sink — это фильтр на основе Кспрокси в режиме ядра. Он используется в аналоговых графах фильтра видео, где данные ВБИ подготавливаются к просмотру или записи. Фильтр подключен к [фильтру записи видео WDM](wdm-video-capture-filter.md) и предоставляет эффективные средства для дублирования потоков данных в режиме ядра без дорогостоящих переходов между режимами ядра и пользователя. Он доставляет каждый полученный блок данных во все выходные сигналы, а нисходящий кодек отвечает за поиск конкретных ВБИ данных для декодирования.

Преобразователь tee/Sink-to-Sink отображается в категории фильтра "WDM Streaming tee/Splitter Devices" ( \_ \_ Разделитель кскатегори).

Так как это фильтр режима ядра, приложения не могут создать его напрямую с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Вместо этого используйте [перечислитель системных устройств](system-device-enumerator.md). Дополнительные сведения см. в разделе [Создание фильтров Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 
