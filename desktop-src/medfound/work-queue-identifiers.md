---
description: Следующие константы обозначают стандартные Media Foundation рабочие очереди.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Идентификаторы рабочих очередей (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663485"
---
# <a name="work-queue-identifiers"></a>Идентификаторы рабочей очереди

Следующие константы обозначают стандартные Media Foundation рабочие очереди.

Приложения должны использовать \_ многопоточность очереди обратного вызова мфасинк \_ \_ или использовать рабочую очередь, полученную от [**мфлоккшаредворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) , если им требуется управлять приоритетом выполнения. Обратите внимание, что приоритеты рабочих очередей рабочей очереди по умолчанию могут динамически изменяться, когда приложение вызывает [**регистерплатформвисммксс**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss). Дополнительные сведения о рабочих очередях см. в разделе [рабочие очереди](work-queues.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">В большинстве случаев приложения должны использовать <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br/> Эта Рабочая очередь используется для синхронных операций. Использование стандартной рабочей очереди может вызвать риск взаимоблокировки. Приложения могут создать частную синхронную очередь поверх многопоточной очереди с помощью <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>мфаллокатесериалворккуеуе</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Не для общего использования приложения.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </dl></td>
<td style="text-align: left;">Не для общего использования приложения.<br/> Эта Рабочая очередь используется для внутренних операций ввода-вывода, таких как чтение файлов и чтение из сети.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Не для общего использования приложения.<br/> Эта Рабочая очередь используется для периодических обратных вызовов и запланированных рабочих элементов. Следующие функции помещают рабочие элементы в эту очередь:<br/>
<ul>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>мфаддпериодиккаллбакк</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>мфсчедулеворкитем</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>мфсчедулеворкитемекс</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </dl></td>
<td style="text-align: left;">В большинстве случаев следует использовать эту многопоточные рабочие очереди. <br/> Эта Рабочая очередь используется для асинхронных операций в Media Foundation.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </dl></td>
<td style="text-align: left;">Не для общего использования приложения. Вместо этого приложения должны использовать <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br/></td>
</tr>
</tbody>
</table>



Кроме того, в связи с рабочими очередями используются следующие константы.



| Константа/значение                                                                                                                                                                                                                                                                                     | Описание                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**Мфасинк \_ Очередь ОБРАТНОго вызова не \_ \_ определена**</dt> <dt>0x00000000</dt> </dl>           | Неопределенная Рабочая очередь.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**Мфасинк \_ 0xFFFF0000 \_ \_ Частная \_ Маска очереди обратного вызова**</dt> <dt></dt> </dl> | Битовая маска для различения рабочих очередей платформы, созданных путем вызова [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Для рабочей очереди, созданной с помощью [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), следующее значение не равно нулю:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**Мфасинк \_ Очередь ОБРАТНОго вызова \_ \_ все**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Все рабочие очереди платформы.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы Media Foundation](media-foundation-constants.md)
</dt> <dt>

[Рабочие очереди](work-queues.md)
</dt> <dt>

[Усовершенствования рабочей очереди и потоков](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




