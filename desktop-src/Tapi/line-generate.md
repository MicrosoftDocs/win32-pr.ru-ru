---
description: '\_Сообщение о формировании линии TAPI отправляется, чтобы уведомить приложение о завершении текущей разрядности или формирования тона.'
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Сообщение LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689121"
---
# <a name="line_generate-message"></a><span data-ttu-id="d832e-103">\_Сообщение создания строки</span><span class="sxs-lookup"><span data-stu-id="d832e-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="d832e-104">Сообщение о **\_ формировании линии** TAPI отправляется, чтобы уведомить приложение о завершении текущей разрядности или формирования тона.</span><span class="sxs-lookup"><span data-stu-id="d832e-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="d832e-105">Только один такой запрос на создание может находиться в процессе выполнения данного вызова в любое время.</span><span class="sxs-lookup"><span data-stu-id="d832e-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="d832e-106">Это сообщение также отправляется при отмене создания цифр или тонов.</span><span class="sxs-lookup"><span data-stu-id="d832e-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d832e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d832e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d832e-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="d832e-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d832e-109">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="d832e-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="d832e-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="d832e-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d832e-111">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="d832e-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="d832e-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d832e-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d832e-113">Причина прекращения создания цифры или тона.</span><span class="sxs-lookup"><span data-stu-id="d832e-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="d832e-114">Этот параметр должен быть одной и только одной из [**\_ констант линеженератетерм**](linegenerateterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d832e-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d832e-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d832e-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d832e-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d832e-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d832e-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d832e-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d832e-118">Число тактов (число миллисекунд с момента запуска Windows), на которых было выполнено создание цифр или тонов.</span><span class="sxs-lookup"><span data-stu-id="d832e-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="d832e-119">Для версий API, предшествующих 2,0, этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="d832e-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d832e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d832e-120">Return value</span></span>

<span data-ttu-id="d832e-121">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d832e-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d832e-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d832e-122">Remarks</span></span>

<span data-ttu-id="d832e-123">Сообщение **о \_ формировании строки** отправляется приложению, которое запросило создание цифры или тона.</span><span class="sxs-lookup"><span data-stu-id="d832e-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="d832e-124">Так как отметка времени, заданная параметром *dwParam3* , может быть создана на компьютере, отличном от того, на котором выполняется приложение, оно полезно только для сравнения с другими подобными сообщениями с метками времени, созданными на том же устройстве ( [**строка \_ гасердигитс**](line-gatherdigits.md), [**строка \_ монитордигитс**](line-monitordigits.md), [**строка \_ монитормедиа**](line-monitormedia.md), [**строка \_ монитортоне**](line-monitortone.md)), чтобы определить их относительное время (разделение между событиями).</span><span class="sxs-lookup"><span data-stu-id="d832e-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="d832e-125">После приблизительно 49,7 дней счетчик тактов может быть заключен в оболочку. приложения должны учитывать это при выполнении вычислений.</span><span class="sxs-lookup"><span data-stu-id="d832e-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="d832e-126">Если поставщик услуг не создает отметку времени (например, если она была создана с помощью более ранней версии TAPI), TAPI предоставляет метку времени в ближайшем к поставщику услуге, который создает событие, чтобы синтезированная метка времени максимально точна.</span><span class="sxs-lookup"><span data-stu-id="d832e-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="d832e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d832e-127">Requirements</span></span>



| <span data-ttu-id="d832e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d832e-128">Requirement</span></span> | <span data-ttu-id="d832e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d832e-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d832e-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d832e-130">TAPI version</span></span><br/> | <span data-ttu-id="d832e-131">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d832e-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d832e-132">Header</span><span class="sxs-lookup"><span data-stu-id="d832e-132">Header</span></span><br/>       | <dl> <span data-ttu-id="d832e-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d832e-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d832e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d832e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d832e-135">**Строка \_ гасердигитс**</span><span class="sxs-lookup"><span data-stu-id="d832e-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="d832e-136">**Строка \_ монитордигитс**</span><span class="sxs-lookup"><span data-stu-id="d832e-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="d832e-137">**Строка \_ монитормедиа**</span><span class="sxs-lookup"><span data-stu-id="d832e-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="d832e-138">**Строка \_ монитортоне**</span><span class="sxs-lookup"><span data-stu-id="d832e-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




