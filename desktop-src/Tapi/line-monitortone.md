---
description: Сообщение TAPI LINE \_ монитортоне отправляется при обнаружении тона. Отправка этого сообщения контролируется с помощью функции Линемонитортонес.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Сообщение LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679868"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="57cda-104">Строка \_ сообщения монитортоне</span><span class="sxs-lookup"><span data-stu-id="57cda-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="57cda-105">Сообщение TAPI **Line \_ монитортоне** отправляется при обнаружении тона.</span><span class="sxs-lookup"><span data-stu-id="57cda-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="57cda-106">Отправка этого сообщения контролируется с помощью функции [**линемонитортонес**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .</span><span class="sxs-lookup"><span data-stu-id="57cda-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="57cda-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="57cda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cda-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="57cda-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="57cda-109">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="57cda-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="57cda-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="57cda-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="57cda-111">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="57cda-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="57cda-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="57cda-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="57cda-113">Зависящий от приложения элемент **дваппспеЦифик** структуры [**линемонитортоне**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) для обнаруженного сигнала.</span><span class="sxs-lookup"><span data-stu-id="57cda-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="57cda-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="57cda-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="57cda-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="57cda-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="57cda-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="57cda-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="57cda-117">Число тактов (число миллисекунд с момента запуска Windows), в которых был обнаружен тон.</span><span class="sxs-lookup"><span data-stu-id="57cda-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="57cda-118">Для версий API, предшествующих 2,0, этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="57cda-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cda-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57cda-119">Return value</span></span>

<span data-ttu-id="57cda-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="57cda-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57cda-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57cda-121">Remarks</span></span>

<span data-ttu-id="57cda-122">Сообщение **Line \_ монитортоне** отправляется только в приложение, которое запросило мониторинг тона.</span><span class="sxs-lookup"><span data-stu-id="57cda-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="57cda-123">Так как эта метка времени могла быть создана на компьютере, отличном от того, на котором выполняется приложение, оно полезно только для сравнения с другими подобными сообщениями с метками времени, созданными на том же устройстве ( [**строка \_ гасердигитс**](line-gatherdigits.md), [**строка \_ Generate**](line-generate.md), [**строка \_ монитордигитс**](line-monitordigits.md), **\_ монитортоне**), чтобы определить их относительную временную шкалу (разделение между событиями).</span><span class="sxs-lookup"><span data-stu-id="57cda-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="57cda-124">После приблизительно 49,7 дней счетчик тактов может быть заключен в оболочку. приложения должны учитывать это при выполнении вычислений.</span><span class="sxs-lookup"><span data-stu-id="57cda-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="57cda-125">Если поставщик услуг не создает отметку времени (например, если она была создана с помощью более ранней версии TAPI), TAPI предоставляет метку времени в ближайшем к поставщику услуге, который создает событие, чтобы синтезированная метка времени максимально точна.</span><span class="sxs-lookup"><span data-stu-id="57cda-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cda-126">Требования</span><span class="sxs-lookup"><span data-stu-id="57cda-126">Requirements</span></span>



| <span data-ttu-id="57cda-127">Требование</span><span class="sxs-lookup"><span data-stu-id="57cda-127">Requirement</span></span> | <span data-ttu-id="57cda-128">Значение</span><span class="sxs-lookup"><span data-stu-id="57cda-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="57cda-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="57cda-129">TAPI version</span></span><br/> | <span data-ttu-id="57cda-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="57cda-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="57cda-131">Header</span><span class="sxs-lookup"><span data-stu-id="57cda-131">Header</span></span><br/>       | <dl> <span data-ttu-id="57cda-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="57cda-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57cda-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57cda-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cda-134">**Строка \_ гасердигитс**</span><span class="sxs-lookup"><span data-stu-id="57cda-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="57cda-135">**\_Создание строки**</span><span class="sxs-lookup"><span data-stu-id="57cda-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="57cda-136">**Строка \_ монитордигитс**</span><span class="sxs-lookup"><span data-stu-id="57cda-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="57cda-137">**линемонитортоне**</span><span class="sxs-lookup"><span data-stu-id="57cda-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="57cda-138">**линемонитортонес**</span><span class="sxs-lookup"><span data-stu-id="57cda-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




