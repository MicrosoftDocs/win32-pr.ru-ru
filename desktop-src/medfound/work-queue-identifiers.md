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
# <a name="work-queue-identifiers"></a><span data-ttu-id="0a0a1-103">Идентификаторы рабочей очереди</span><span class="sxs-lookup"><span data-stu-id="0a0a1-103">Work Queue Identifiers</span></span>

<span data-ttu-id="0a0a1-104">Следующие константы обозначают стандартные Media Foundation рабочие очереди.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="0a0a1-105">Приложения должны использовать \_ многопоточность очереди обратного вызова мфасинк \_ \_ или использовать рабочую очередь, полученную от [**мфлоккшаредворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) , если им требуется управлять приоритетом выполнения.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="0a0a1-106">Обратите внимание, что приоритеты рабочих очередей рабочей очереди по умолчанию могут динамически изменяться, когда приложение вызывает [**регистерплатформвисммксс**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span><span class="sxs-lookup"><span data-stu-id="0a0a1-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="0a0a1-107">Дополнительные сведения о рабочих очередях см. в разделе [рабочие очереди](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="0a0a1-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0a0a1-108">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="0a0a1-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0a0a1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0a0a1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="0a0a1-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="0a0a1-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0a0a1-111">В большинстве случаев приложения должны использовать <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="0a0a1-112">Эта Рабочая очередь используется для синхронных операций.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="0a0a1-113">Использование стандартной рабочей очереди может вызвать риск взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="0a0a1-114">Приложения могут создать частную синхронную очередь поверх многопоточной очереди с помощью <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>мфаллокатесериалворккуеуе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="0a0a1-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="0a0a1-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0a0a1-116">Не для общего использования приложения.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="0a0a1-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="0a0a1-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0a0a1-118">Не для общего использования приложения.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-118">Not for general application use.</span></span><br/> <span data-ttu-id="0a0a1-119">Эта Рабочая очередь используется для внутренних операций ввода-вывода, таких как чтение файлов и чтение из сети.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="0a0a1-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="0a0a1-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0a0a1-121">Не для общего использования приложения.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-121">Not for general application use.</span></span><br/> <span data-ttu-id="0a0a1-122">Эта Рабочая очередь используется для периодических обратных вызовов и запланированных рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="0a0a1-123">Следующие функции помещают рабочие элементы в эту очередь:</span><span class="sxs-lookup"><span data-stu-id="0a0a1-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="0a0a1-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>мфаддпериодиккаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a0a1-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="0a0a1-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>мфсчедулеворкитем</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a0a1-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="0a0a1-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>мфсчедулеворкитемекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a0a1-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="0a0a1-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span><span class="sxs-lookup"><span data-stu-id="0a0a1-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0a0a1-128">В большинстве случаев следует использовать эту многопоточные рабочие очереди.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="0a0a1-129">Эта Рабочая очередь используется для асинхронных операций в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="0a0a1-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="0a0a1-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="0a0a1-131">Не для общего использования приложения.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-131">Not for general application use.</span></span> <span data-ttu-id="0a0a1-132">Вместо этого приложения должны использовать <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="0a0a1-133">Кроме того, в связи с рабочими очередями используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="0a0a1-134">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="0a0a1-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0a0a1-135">Описание</span><span class="sxs-lookup"><span data-stu-id="0a0a1-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="0a0a1-136"><dt>**Мфасинк \_ Очередь ОБРАТНОго вызова не \_ \_ определена**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0a0a1-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="0a0a1-137">Неопределенная Рабочая очередь.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="0a0a1-138"><dt>**Мфасинк \_ 0xFFFF0000 \_ \_ Частная \_ Маска очереди обратного вызова**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0a0a1-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="0a0a1-139">Битовая маска для различения рабочих очередей платформы, созданных путем вызова [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="0a0a1-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="0a0a1-140">Для рабочей очереди, созданной с помощью [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), следующее значение не равно нулю:</span><span class="sxs-lookup"><span data-stu-id="0a0a1-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="0a0a1-141"><dt>**Мфасинк \_ Очередь ОБРАТНОго вызова \_ \_ все**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="0a0a1-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="0a0a1-142">Все рабочие очереди платформы.</span><span class="sxs-lookup"><span data-stu-id="0a0a1-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="0a0a1-143">Требования</span><span class="sxs-lookup"><span data-stu-id="0a0a1-143">Requirements</span></span>



| <span data-ttu-id="0a0a1-144">Требование</span><span class="sxs-lookup"><span data-stu-id="0a0a1-144">Requirement</span></span> | <span data-ttu-id="0a0a1-145">Значение</span><span class="sxs-lookup"><span data-stu-id="0a0a1-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0a1-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a0a1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0a0a1-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a0a1-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0a0a1-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a0a1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0a0a1-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a0a1-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a0a1-150">Header</span><span class="sxs-lookup"><span data-stu-id="0a0a1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a0a1-151"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a0a1-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a0a1-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a0a1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0a1-153">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a0a1-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="0a0a1-154">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="0a0a1-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="0a0a1-155">Усовершенствования рабочей очереди и потоков</span><span class="sxs-lookup"><span data-stu-id="0a0a1-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




