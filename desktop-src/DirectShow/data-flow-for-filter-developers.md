---
description: Flow данных для разработчиков фильтров
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Flow данных для разработчиков фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ced9507856d7a6b8aea2acaea86c20b393b8d937ab4427bf522596a29ba690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749374"
---
# <a name="data-flow-for-filter-developers"></a>Flow данных для разработчиков фильтров

В этом разделе подробно описывается перемещение данных с помощью графа фильтра. Он посвящен транспорту локальной памяти с помощью интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) или [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Он предназначен для разработчиков, создающих собственные настраиваемые фильтры. общие сведения о том, как Microsoft DirectShow обрабатывает поток данных, см. в разделе [Flow данных в Graph фильтров](data-flow-in-the-filter-graph.md).

Большое количество данных перемещается через граф фильтра. Он делится на две категории: данные мультимедиа и управляющие данные. Как правило, данные мультимедиа перемещаются в нисходящий поток, а управление данными перемещается вверх. Данные мультимедиа включают видеокадры, образцы аудио, пакеты MPEG и так далее, которые составляют поток, но также включают команды Flush, уведомления конца потока и другие данные, передаваемые в поток. Управляющие данные не являются частью потока мультимедиа. Примерами управляющих данных являются запросы контроля качества и команды поиска.

Этот раздел содержит следующие статьи.

-   [Доставка образцов](delivering-samples.md)
-   [Обработка данных](processing-data.md)
-   [Уведомления о завершении потока](end-of-stream-notifications.md)
-   [Новые сегменты](new-segments.md)
-   [Очистки](flushing.md)
-   [Нужна](seeking.md)
-   [Изменения динамического формата](dynamic-format-changes.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление качеством](quality-control-management.md)
</dt> <dt>

[Потоки и критические разделы](threads-and-critical-sections.md)
</dt> <dt>

[написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



