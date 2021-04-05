---
description: Поток данных для разработчиков фильтров
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Поток данных для разработчиков фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072314"
---
# <a name="data-flow-for-filter-developers"></a>Поток данных для разработчиков фильтров

В этом разделе подробно описывается перемещение данных с помощью графа фильтра. Он посвящен транспорту локальной памяти с помощью интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) или [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Он предназначен для разработчиков, создающих собственные настраиваемые фильтры. Общие сведения о том, как Microsoft DirectShow обрабатывает поток данных, см. [в разделе поток данных в графе фильтра](data-flow-in-the-filter-graph.md).

Большое количество данных перемещается через граф фильтра. Он делится на две категории: данные мультимедиа и управляющие данные. Как правило, данные мультимедиа перемещаются в нисходящий поток, а управление данными перемещается вверх. Данные мультимедиа включают видеокадры, образцы аудио, пакеты MPEG и так далее, которые составляют поток, но также включают команды Flush, уведомления конца потока и другие данные, передаваемые в поток. Управляющие данные не являются частью потока мультимедиа. Примерами управляющих данных являются запросы контроля качества и команды поиска.

Этот раздел содержит следующие статьи.

-   [Доставка образцов](delivering-samples.md)
-   [Обработка данных](processing-data.md)
-   [Уведомления о завершении потока](end-of-stream-notifications.md)
-   [Новые сегменты](new-segments.md)
-   [Очистки](flushing.md)
-   [Нужна](seeking.md)
-   [Изменения динамического формата](dynamic-format-changes.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление качеством](quality-control-management.md)
</dt> <dt>

[Потоки и критические разделы](threads-and-critical-sections.md)
</dt> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



