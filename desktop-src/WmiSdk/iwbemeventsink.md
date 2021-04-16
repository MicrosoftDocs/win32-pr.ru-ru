---
description: Инициирует связь с поставщиком событий с помощью ограниченного набора запросов.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Интерфейс Ивбемевентсинк (Вбемпров. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702749"
---
# <a name="iwbemeventsink-interface"></a><span data-ttu-id="eb9f8-103">Интерфейс Ивбемевентсинк</span><span class="sxs-lookup"><span data-stu-id="eb9f8-103">IWbemEventSink interface</span></span>

<span data-ttu-id="eb9f8-104">Интерфейс **ивбемевентсинк** инициирует связь с поставщиком событий с помощью ограниченного набора запросов.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-104">The **IWbemEventSink** interface initiates communication with an event provider using a restricted set of queries.</span></span> <span data-ttu-id="eb9f8-105">Этот интерфейс расширяет [**ивбемобжектсинк**](iwbemobjectsink.md), предоставляя новые методы, работающие с безопасностью и производительностью.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-105">This interface extends [**IWbemObjectSink**](iwbemobjectsink.md), providing new methods dealing with security and performance.</span></span> <span data-ttu-id="eb9f8-106">Дополнительные сведения об использовании этого интерфейса см. в разделе [написание поставщика событий](writing-an-event-provider.md) и [обеспечение безопасности событий WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="eb9f8-106">For more information about using this interface, see [Writing an Event Provider](writing-an-event-provider.md) and [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="members"></a><span data-ttu-id="eb9f8-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="eb9f8-107">Members</span></span>

<span data-ttu-id="eb9f8-108">Интерфейс **ивбемевентсинк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eb9f8-108">The **IWbemEventSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="eb9f8-109">Методы</span><span class="sxs-lookup"><span data-stu-id="eb9f8-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eb9f8-110">Методы</span><span class="sxs-lookup"><span data-stu-id="eb9f8-110">Methods</span></span>

<span data-ttu-id="eb9f8-111">Интерфейс **ивбемевентсинк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-111">The **IWbemEventSink** interface has these methods.</span></span>



| <span data-ttu-id="eb9f8-112">Метод</span><span class="sxs-lookup"><span data-stu-id="eb9f8-112">Method</span></span>                                                                | <span data-ttu-id="eb9f8-113">Описание</span><span class="sxs-lookup"><span data-stu-id="eb9f8-113">Description</span></span>                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="eb9f8-114">**жетрестриктедсинк**</span><span class="sxs-lookup"><span data-stu-id="eb9f8-114">**GetRestrictedSink**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | <span data-ttu-id="eb9f8-115">Вызывается потребителем для настройки запросов с ограниченными событиями.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-115">Called by the consumer to set up restricted event queries.</span></span><br/> |
| [<span data-ttu-id="eb9f8-116">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="eb9f8-116">**IsActive**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | <span data-ttu-id="eb9f8-117">Проверяет состояние приемника событий.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-117">Checks status of event sink.</span></span><br/>                               |
| [<span data-ttu-id="eb9f8-118">**сетбатчингпараметерс**</span><span class="sxs-lookup"><span data-stu-id="eb9f8-118">**SetBatchingParameters**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | <span data-ttu-id="eb9f8-119">Вызывается потребителем для задания пакетных параметров.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-119">Called by the consumer to set batching parameters.</span></span><br/>         |
| [<span data-ttu-id="eb9f8-120">**сетсинксекурити**</span><span class="sxs-lookup"><span data-stu-id="eb9f8-120">**SetSinkSecurity**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | <span data-ttu-id="eb9f8-121">Используется для обновления дескриптора безопасности в приемнике событий.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-121">Used to update the security descriptor on an event sink.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="eb9f8-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb9f8-122">Remarks</span></span>

<span data-ttu-id="eb9f8-123">При реализации приемника подписки на события ([**ивбемобжектсинк**](iwbemobjectsink.md) или **ивбемевентсинк**) не следует вызывать WMI из методов объекта приемника.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-123">When implementing an event subscription sink ([**IWbemObjectSink**](iwbemobjectsink.md) or **IWbemEventSink**), do not call into WMI from within the methods on the sink object.</span></span> <span data-ttu-id="eb9f8-124">Например, вызов [**IWbemServices:: канцеласинккалл**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) для отмены приемника из реализации [**Ивбемевентсинк:: сетсинксекурити**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) может повлиять на состояние WMI.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-124">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) can interfere with the WMI state.</span></span> <span data-ttu-id="eb9f8-125">Чтобы отменить подписку на события, установите флаг и вызовите **IWbemServices:: канцеласинккалл** из другого потока или объекта.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-125">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="eb9f8-126">Для реализаций, которые не связаны с приемником событий, например объектом, перечислением и получением запросов, можно выполнить обратный вызов к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-126">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="eb9f8-127">Реализации приемника должны обрабатывать уведомление о событии в течение 100 мс, поскольку поток WMI, доставляющий уведомление о событии, не может выполнить другие действия, пока объект приемника не завершит обработку.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-127">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="eb9f8-128">Если для уведомления требуется большой объем обработки, приемник может использовать внутреннюю очередь для другого потока, чтобы обработать обработку.</span><span class="sxs-lookup"><span data-stu-id="eb9f8-128">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9f8-129">Требования</span><span class="sxs-lookup"><span data-stu-id="eb9f8-129">Requirements</span></span>



| <span data-ttu-id="eb9f8-130">Требование</span><span class="sxs-lookup"><span data-stu-id="eb9f8-130">Requirement</span></span> | <span data-ttu-id="eb9f8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eb9f8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9f8-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb9f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9f8-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb9f8-133">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="eb9f8-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb9f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9f8-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb9f8-135">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="eb9f8-136">Header</span><span class="sxs-lookup"><span data-stu-id="eb9f8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb9f8-137"><dt>Вбемпров. h (включение Вбемидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb9f8-137"><dt>Wbemprov.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="eb9f8-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eb9f8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb9f8-139"><dt>Вбемууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb9f8-139"><dt>Wbemuuid.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="eb9f8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="eb9f8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb9f8-141"><dt>Wbemsvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9f8-141"><dt>Wbemsvc.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="eb9f8-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb9f8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9f8-143">COM API для WMI</span><span class="sxs-lookup"><span data-stu-id="eb9f8-143">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

 




