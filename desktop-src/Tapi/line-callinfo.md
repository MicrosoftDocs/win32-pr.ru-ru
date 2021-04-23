---
description: Сообщение TAPI LINE \_ каллинфо отправляется при изменении сведений о вызове указанного вызова. Приложение может вызвать Линежеткаллинфо для определения текущих сведений о вызовах.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Сообщение LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688823"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="c6575-104">Строка \_ сообщения каллинфо</span><span class="sxs-lookup"><span data-stu-id="c6575-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="c6575-105">Сообщение TAPI **Line \_ каллинфо** отправляется при изменении сведений о вызове указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="c6575-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="c6575-106">Приложение может вызвать [**линежеткаллинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) для определения текущих сведений о вызовах.</span><span class="sxs-lookup"><span data-stu-id="c6575-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c6575-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6575-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6575-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="c6575-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c6575-109">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="c6575-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="c6575-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="c6575-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="c6575-111">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="c6575-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="c6575-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c6575-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="c6575-113">Измененный элемент сведений о вызове.</span><span class="sxs-lookup"><span data-stu-id="c6575-113">The call information item that has changed.</span></span> <span data-ttu-id="c6575-114">Может быть одной или несколькими [**\_ константами линекаллинфостате**](linecallinfostate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="c6575-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6575-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c6575-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="c6575-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c6575-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c6575-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="c6575-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="c6575-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c6575-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6575-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6575-119">Return value</span></span>

<span data-ttu-id="c6575-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c6575-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6575-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6575-121">Remarks</span></span>

<span data-ttu-id="c6575-122">**Строка сообщения \_ каллинфо** с указанием *нумовнерсинкр*, *нумовнерсдекр* и (или) *нуммониторсчанжед* отправляется в приложения, которые уже имеют обработчик для вызова.</span><span class="sxs-lookup"><span data-stu-id="c6575-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="c6575-123">Это может быть результатом того, что другое приложение изменяет владельца или отслеживание на вызов с помощью [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**линесеткаллпривилеже**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**линежетневкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)и [**линежетконфрелатедкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span><span class="sxs-lookup"><span data-stu-id="c6575-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="c6575-124">Эти **строки \_ каллинфо** сообщения не отправляются, если уведомление о новом вызове предоставляется в [**строке \_ каллстате**](line-callstate.md) , поскольку сведения о вызове уже отражают правильное количество владельцев и мониторов на момент \_ отправки строки каллстате сообщений.</span><span class="sxs-lookup"><span data-stu-id="c6575-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="c6575-125">**Строка \_ Сообщения КАЛЛИНФО** также подавляются в случае, когда интерфейс TAPI предоставляет вызов для мониторинга через линекаллстате \_ неизвестный механизм.</span><span class="sxs-lookup"><span data-stu-id="c6575-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="c6575-126">Приложение, которое вызывает изменение числа владельцев или мониторов (например, путем вызова [**линедеаллокатекалл**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) или [**линесеткаллпривилеже**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)), само по себе не получает сообщение о том, что изменение выполнено.</span><span class="sxs-lookup"><span data-stu-id="c6575-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="c6575-127">Сообщения **\_ каллинфо Line** не отправляются для вызова после того, как вызов перешел в состояние *простоя* .</span><span class="sxs-lookup"><span data-stu-id="c6575-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="c6575-128">В частности, изменения в количестве владельцев и мониторов не отображаются, так как приложения отменяют выделение своих дескрипторов для неактивного вызова.</span><span class="sxs-lookup"><span data-stu-id="c6575-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6575-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c6575-129">Requirements</span></span>



| <span data-ttu-id="c6575-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c6575-130">Requirement</span></span> | <span data-ttu-id="c6575-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c6575-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c6575-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="c6575-132">TAPI version</span></span><br/> | <span data-ttu-id="c6575-133">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c6575-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c6575-134">Header</span><span class="sxs-lookup"><span data-stu-id="c6575-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c6575-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6575-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6575-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6575-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6575-137">**линеклосе**</span><span class="sxs-lookup"><span data-stu-id="c6575-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="c6575-138">**линедеаллокатекалл**</span><span class="sxs-lookup"><span data-stu-id="c6575-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="c6575-139">**линежеткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="c6575-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="c6575-140">**линежетконфрелатедкаллс**</span><span class="sxs-lookup"><span data-stu-id="c6575-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="c6575-141">**линежетневкаллс**</span><span class="sxs-lookup"><span data-stu-id="c6575-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="c6575-142">**линеопен**</span><span class="sxs-lookup"><span data-stu-id="c6575-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="c6575-143">**линесеткаллпривилеже**</span><span class="sxs-lookup"><span data-stu-id="c6575-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="c6575-144">**линешутдовн**</span><span class="sxs-lookup"><span data-stu-id="c6575-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




