---
description: '\_Сообщение ГАСЕРДИГИТС линии TAPI отправляется, когда текущий запрос на буферизацию разрядности был завершен или отменен. Буфер цифр можно исследовать после получения этого сообщения приложением.'
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Сообщение LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675374"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="7620b-104">Строка \_ сообщения гасердигитс</span><span class="sxs-lookup"><span data-stu-id="7620b-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="7620b-105">Сообщение **\_ ГАСЕРДИГИТС линии** TAPI отправляется, когда текущий запрос на буферизацию разрядности был завершен или отменен.</span><span class="sxs-lookup"><span data-stu-id="7620b-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="7620b-106">Буфер цифр можно исследовать после получения этого сообщения приложением.</span><span class="sxs-lookup"><span data-stu-id="7620b-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7620b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7620b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7620b-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="7620b-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7620b-109">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="7620b-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="7620b-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="7620b-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7620b-111">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="7620b-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="7620b-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7620b-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7620b-113">Причина прекращения сбора цифр.</span><span class="sxs-lookup"><span data-stu-id="7620b-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="7620b-114">Этот параметр должен быть одной и только одной из [**\_ констант линегасертерм**](linegatherterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7620b-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7620b-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7620b-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7620b-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7620b-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7620b-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7620b-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7620b-118">Число тактов (число миллисекунд с момента запуска Windows), с которых выполняется сбор цифр.</span><span class="sxs-lookup"><span data-stu-id="7620b-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="7620b-119">Для TAPI версий более ранних, чем 2,0, этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7620b-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7620b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7620b-120">Return value</span></span>

<span data-ttu-id="7620b-121">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="7620b-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7620b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7620b-122">Remarks</span></span>

<span data-ttu-id="7620b-123">Сообщение **Line \_ гасердигитс** отправляется в приложение, которое инициировало сбор цифр при вызове с помощью [**линегасердигитс**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span><span class="sxs-lookup"><span data-stu-id="7620b-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="7620b-124">Если функция [**линегасердигитс**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) используется для отмены предыдущего запроса для получения цифр, TAPI отправляет сообщение **Line \_ Гасердигитс** с параметром *dwParam1* , равным линегасертерм Cancel, в \_ приложение, указывающее, что первоначально указанный буфер содержит цифры, собранные до отмены.</span><span class="sxs-lookup"><span data-stu-id="7620b-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="7620b-125">Так как отметка времени, заданная параметром *dwParam3* , может быть создана на компьютере, отличном от того, на котором выполняется приложение, он полезен только для сравнения с другими подобными сообщениями с метками времени, созданными на том же устройстве ( [**строка \_ Generate**](line-generate.md), [**строка \_ монитордигитс**](line-monitordigits.md), [**строка \_ монитормедиа**](line-monitormedia.md), [**строка \_ монитортоне**](line-monitortone.md)), чтобы определить их относительное время (разделение между событиями).</span><span class="sxs-lookup"><span data-stu-id="7620b-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="7620b-126">После приблизительно 49,7 дней счетчик тактов может быть заключен в оболочку. приложения должны учитывать это при выполнении вычислений.</span><span class="sxs-lookup"><span data-stu-id="7620b-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="7620b-127">Если поставщик услуг не создает отметку времени (например, если она была создана с помощью более ранней версии TAPI), TAPI предоставляет метку времени в ближайшем к поставщику услуге, который создает событие, чтобы синтезированная метка времени максимально точна.</span><span class="sxs-lookup"><span data-stu-id="7620b-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="7620b-128">Когда приложение вызывает любую асинхронную операцию, которая записывает данные обратно в память приложения, приложение должно обеспечить доступность памяти для записи, пока не будет получено сообщение [**строки \_ Reply**](line-reply.md) или **Line \_ гасердигитс** .</span><span class="sxs-lookup"><span data-stu-id="7620b-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7620b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="7620b-129">Requirements</span></span>



| <span data-ttu-id="7620b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="7620b-130">Requirement</span></span> | <span data-ttu-id="7620b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7620b-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7620b-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7620b-132">TAPI version</span></span><br/> | <span data-ttu-id="7620b-133">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7620b-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7620b-134">Header</span><span class="sxs-lookup"><span data-stu-id="7620b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="7620b-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7620b-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7620b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7620b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7620b-137">**\_Создание строки**</span><span class="sxs-lookup"><span data-stu-id="7620b-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="7620b-138">**Строка \_ монитордигитс**</span><span class="sxs-lookup"><span data-stu-id="7620b-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="7620b-139">**Строка \_ монитормедиа**</span><span class="sxs-lookup"><span data-stu-id="7620b-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="7620b-140">**Строка \_ монитортоне**</span><span class="sxs-lookup"><span data-stu-id="7620b-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="7620b-141">**\_ответ строки**</span><span class="sxs-lookup"><span data-stu-id="7620b-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="7620b-142">**линегасердигитс**</span><span class="sxs-lookup"><span data-stu-id="7620b-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




