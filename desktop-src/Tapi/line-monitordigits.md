---
description: '\_Сообщение МОНИТОРДИГИТС линии TAPI отправляется при обнаружении цифры. Отправка этого сообщения контролируется с помощью функции Линемонитордигитс.'
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Сообщение LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675566"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="96798-104">Строка \_ сообщения монитордигитс</span><span class="sxs-lookup"><span data-stu-id="96798-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="96798-105">Сообщение **\_ МОНИТОРДИГИТС линии** TAPI отправляется при обнаружении цифры.</span><span class="sxs-lookup"><span data-stu-id="96798-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="96798-106">Отправка этого сообщения контролируется с помощью функции [**линемонитордигитс**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .</span><span class="sxs-lookup"><span data-stu-id="96798-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="96798-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="96798-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96798-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="96798-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="96798-109">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="96798-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="96798-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="96798-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="96798-111">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="96798-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="96798-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="96798-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="96798-113">Байт нижнего порядка содержит последнюю цифру, полученную в текстовом представлении.</span><span class="sxs-lookup"><span data-stu-id="96798-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="96798-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="96798-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="96798-115">Обнаруженный цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="96798-115">The digit mode that was detected.</span></span> <span data-ttu-id="96798-116">Этот параметр должен быть одной и только одной из [**\_ констант линедигитмоде**](linedigitmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="96798-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="96798-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="96798-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="96798-118">Число тактов (число миллисекунд с момента запуска Windows), в которых была обнаружена указанная цифра.</span><span class="sxs-lookup"><span data-stu-id="96798-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="96798-119">Для TAPI версий более ранних, чем 2,0, этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="96798-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96798-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96798-120">Return value</span></span>

<span data-ttu-id="96798-121">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="96798-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96798-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96798-122">Remarks</span></span>

<span data-ttu-id="96798-123">**Строка \_ монитордигитс** отправляется в приложение с включенным отслеживанием цифр.</span><span class="sxs-lookup"><span data-stu-id="96798-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="96798-124">Так как эта метка времени могла быть создана на компьютере, отличном от того, на котором выполняется приложение, оно полезно только для сравнения с другими подобными сообщениями с метками времени, созданными на том же устройстве ( [**строка \_ гасердигитс**](line-gatherdigits.md), [**строка \_ Generate**](line-generate.md), [**строка \_ монитормедиа**](line-monitormedia.md), [**\_ монитортоне**](line-monitortone.md)), чтобы определить их относительную временную шкалу (разделение между событиями).</span><span class="sxs-lookup"><span data-stu-id="96798-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="96798-125">После приблизительно 49,7 дней счетчик тактов может быть заключен в оболочку. приложения должны учитывать это при выполнении вычислений.</span><span class="sxs-lookup"><span data-stu-id="96798-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="96798-126">Если поставщик услуг не создает отметку времени (например, если она была создана с помощью более ранней версии TAPI), TAPI предоставляет метку времени в ближайшем к поставщику услуге, который создает событие, чтобы синтезированная метка времени максимально точна.</span><span class="sxs-lookup"><span data-stu-id="96798-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="96798-127">Требования</span><span class="sxs-lookup"><span data-stu-id="96798-127">Requirements</span></span>



| <span data-ttu-id="96798-128">Требование</span><span class="sxs-lookup"><span data-stu-id="96798-128">Requirement</span></span> | <span data-ttu-id="96798-129">Значение</span><span class="sxs-lookup"><span data-stu-id="96798-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="96798-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="96798-130">TAPI version</span></span><br/> | <span data-ttu-id="96798-131">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="96798-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="96798-132">Header</span><span class="sxs-lookup"><span data-stu-id="96798-132">Header</span></span><br/>       | <dl> <span data-ttu-id="96798-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="96798-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96798-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96798-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96798-135">**Строка \_ гасердигитс**</span><span class="sxs-lookup"><span data-stu-id="96798-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="96798-136">**\_Создание строки**</span><span class="sxs-lookup"><span data-stu-id="96798-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="96798-137">**Строка \_ монитормедиа**</span><span class="sxs-lookup"><span data-stu-id="96798-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="96798-138">**Строка \_ монитортоне**</span><span class="sxs-lookup"><span data-stu-id="96798-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="96798-139">**линемонитордигитс**</span><span class="sxs-lookup"><span data-stu-id="96798-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




