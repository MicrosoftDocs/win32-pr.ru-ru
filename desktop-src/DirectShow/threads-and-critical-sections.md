---
description: Потоки и критические разделы
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Потоки и критические разделы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350335"
---
# <a name="threads-and-critical-sections"></a>Потоки и критические разделы

В этом разделе описываются потоки в фильтрах DirectShow, а также действия, которые необходимо выполнить, чтобы избежать сбоев или взаимоблокировок в настраиваемом фильтре.

В примерах, приведенных в этом разделе, для иллюстрации кода, который необходимо написать, используется псевдокод. Они предполагают, что настраиваемый фильтр использует классы, производные от базовых классов DirectShow, следующим образом:

-   Кминпутпин: является производным от [**кбасеинпутпин**](cbaseinputpin.md).
-   Кмйоутпутпин: является производным от [**кбасеаутпутпин**](cbaseoutputpin.md).
-   Кмифилтер: является производным от [**кбасефилтер**](cbasefilter.md).
-   Кминпуталлокатор: распределитель входного контакта, производный от [**кмемаллокатор**](cmemallocator.md). Не каждому фильтру нужен пользовательский распределитель. Для многих фильтров достаточно класса **кмемаллокатор** .

Этот раздел содержит следующие подразделы.

-   [Потоковая передача и потоки приложений](the-streaming-and-application-threads.md)
-   [Переход в режим приостановки](pausing.md)
-   [Получение и доставка примеров](receiving-and-delivering-samples.md)
-   [Доставка конца потока](delivering-the-end-of-stream.md)
-   [Очистка данных](flushing-data.md)
-   [Остановка](stopping.md)
-   [Получение буферов](getting-buffers.md)
-   [Потоковая передача потоков и диспетчер графа фильтров](streaming-threads-and-the-filter-graph-manager.md)
-   [Сводка по потокам фильтров](summary-of-filter-threading.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поток данных для разработчиков фильтров](data-flow-for-filter-developers.md)
</dt> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



