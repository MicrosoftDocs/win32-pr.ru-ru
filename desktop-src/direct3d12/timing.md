---
title: Время (графика Direct3D 12)
description: В этом разделе рассматриваются запросы к отметкам времени и калибровка GPU и счетчиков времени ЦП.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2020
ms.locfileid: "104549041"
---
# <a name="timing-direct3d-12-graphics"></a>Время (графика Direct3D 12)

В этом разделе рассматриваются запросы к отметкам времени и калибровка GPU и счетчиков времени ЦП.

## <a name="timestamp-frequency"></a>Периодичность метки времени

Приложение может запрашивать частоту меток времени GPU для отдельных команд в очереди (см. метод [**ID3D12CommandQueue:: жеттиместампфрекуенци**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).

Возвращаемая частота измеряется в Гц (тактов/с). Если указанная очередь команд не поддерживает метки времени (см. таблицу в разделе [запросов](queries.md) ), то этот API завершается с ошибкой (и возвращает **E_FAIL**). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) и [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) всегда поддерживают метки времени. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) также поддерживает метки времени, если член [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: Копикуеуетиместампкуериессуппортед**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) имеет **значение true**.

## <a name="timestamp-calibration"></a>Калибровка метки времени

D3D12 позволяет приложениям сопоставлять результаты, полученные из запросов меток времени, с результатами, полученными от вызова `QueryPerformanceCounter` . Это можно включить с помощью вызова [**ID3D12CommandQueue:: жетклокккалибратион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**Жетклокккалибратион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) пример счетчика метки времени GPU для заданной очереди команд и одновременное выборка счетчика ЦП `QueryPerformanceCounter` с помощью. \_Если указанная очередь команд не поддерживает метки времени, то этот API завершается ошибкой (возвращается значение E fail) (см. таблицу в разделе [запросов](queries.md) ).

Обратите внимание, что счетчики времени GPU и ЦП не обязательно напрямую связаны с тактовой частотой этих процессоров, а работают с квантами времени.

## <a name="timestamp-queries"></a>Запросы меток времени

Метки времени можно получить как часть списка команд (а не вызова на стороне процессора в очереди команд) с помощью запросов отметок времени. (Общие сведения о запросах см. в разделе [запросы](queries.md) .) 

Все запросы timestamp используют тип [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) для фактического запроса. Однако из-за ограничений, связанных с оборудованием, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) и [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) используют разные [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) , которые [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) использовать.

В очередях Direct и COMPUTE используются [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Очереди копирования используют [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Запросы очереди копирования поддерживаются только в том случае, если элемент [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: копикуеуетиместампкуериессуппортед**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) имеет **значение true**.

Запросы отметок времени после разрешения через [**ID3D12GraphicsCommandList:: ресолвекуеридата**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)являются **UINT64** , представляющими такты, как возвращаемые [**ID3D12CommandQueue:: жетклокккалибратион**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), и поэтому его необходимо разделить частотой очереди для получения длины в секундах.

> [!IMPORTANT]
> Для точности используйте арифметические операции с плавающей запятой при вычислении интервала времени в секундах или миллисекундах. Например, используйте `queriedTicks / (double)Frequency` вместо `queriedTicks / Frequency`.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Счетчики и запросы](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device:: Сетстаблеповерстате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object:: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Измерение производительности](performance-measurement.md)
</dt> </dl>
