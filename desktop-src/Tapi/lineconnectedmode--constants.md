---
description: '\_Константы битового флага линеконнектедмоде описывают различные подсостояния подключенного вызова.'
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Константы LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688924"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="82151-103">\_Константы линеконнектедмоде</span><span class="sxs-lookup"><span data-stu-id="82151-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="82151-104">Константы битового флага **линеконнектедмоде \_** описывают различные подсостояния подключенного вызова.</span><span class="sxs-lookup"><span data-stu-id="82151-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="82151-105">Режим будет доступен в виде состояния вызова для приложения после перехода состояния вызова в состояние "подключено" и в строке \_ каллстате сообщение, указывающее, что вызов находится в линекаллстате \_ Connected.</span><span class="sxs-lookup"><span data-stu-id="82151-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="82151-106">Эти значения используются, когда вызов осуществляется на адресе, который является общим (передается через мост) с другими станциями (Дополнительные сведения см. в разделе [**\_ константы линеаддрессшаринг**](lineaddresssharing--constants.md)), в первую очередь на электронные ключевые системы.</span><span class="sxs-lookup"><span data-stu-id="82151-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="82151-107">**\_ Константы линеконнектедмоде** имеют следующие значения:</span><span class="sxs-lookup"><span data-stu-id="82151-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="82151-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**ЛИНЕКОННЕКТЕДМОДЕ \_ Active**</span><span class="sxs-lookup"><span data-stu-id="82151-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82151-109">Указывает, что вызов подключен к текущей станции (Текущая станция является участником вызова).</span><span class="sxs-lookup"><span data-stu-id="82151-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="82151-110">Если режим вызова равен 0 (нулю), приложение должно предположить, что значение — "активно" (это может быть ситуация на немостном адресе).</span><span class="sxs-lookup"><span data-stu-id="82151-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="82151-111">Режим может переключаться между активными и неактивными во время вызова, если пользователь присоединяется и оставляет вызов с помощью ручного действия.</span><span class="sxs-lookup"><span data-stu-id="82151-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="82151-112">В такой ситуации с мостом операция [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop) или [**линехолд**](/windows/desktop/api/Tapi/nf-tapi-linehold) может не удалить вызов или разместить ее на удержании, так как состояние других станций в вызове может задерживаться (например, при попытке "удержание" вызова, когда участвуют другие станции); Вместо этого вызов можно изменить на неактивный режим, если он остается ПОДКЛЮЧЕНным к другим станциям.</span><span class="sxs-lookup"><span data-stu-id="82151-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82151-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**ЛИНЕКОННЕКТЕДМОДЕ \_ активехелд**</span><span class="sxs-lookup"><span data-stu-id="82151-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82151-114">Указывает, что станция является активным участником в вызове, но удаленная сторона поместила вызов на удержание (другая сторона считает, что вызов находится в состоянии onhold).</span><span class="sxs-lookup"><span data-stu-id="82151-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="82151-115">Как правило, такая информация доступна, только если обе конечные точки вызова попадают в один и тот же домен коммутации.</span><span class="sxs-lookup"><span data-stu-id="82151-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="82151-116">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="82151-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="82151-117">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="82151-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82151-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**ЛИНЕКОННЕКТЕДМОДЕ \_ подтверждено**</span><span class="sxs-lookup"><span data-stu-id="82151-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82151-119">Указывает, что поставщик услуг получил голосами подтверждающими уведомление о том, что вызов перешел в состояние Connected (например, с помощью функции контроля ответов или аналогичных механизмов).</span><span class="sxs-lookup"><span data-stu-id="82151-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="82151-120">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="82151-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="82151-121">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="82151-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82151-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**ЛИНЕКОННЕКТЕДМОДЕ \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="82151-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82151-123">Указывает, что вызов активен на одной или нескольких станциях, но текущая станция не является участником в вызове.</span><span class="sxs-lookup"><span data-stu-id="82151-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="82151-124">Если режим вызова равен нулю, приложение должно предположить, что значение — "активно" (это будет ситуация на немостном адресе).</span><span class="sxs-lookup"><span data-stu-id="82151-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="82151-125">Вызов в неактивном состоянии может быть соединен с помощью [**линеансвер**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="82151-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="82151-126">Многие операции, допустимые в вызовах в ПОДКЛЮЧЕНном состоянии, могут быть невозможными в неактивном режиме, например при мониторинге тонов и цифр, так как станция не участвует в вызове. мониторинг обычно приостанавливается (хотя не отменяется), пока вызов находится в неактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="82151-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82151-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**ЛИНЕКОННЕКТЕДМОДЕ \_ инактивехелд**</span><span class="sxs-lookup"><span data-stu-id="82151-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82151-128">Указывает, что станция не является активным участником в вызове и что удаленная сторона поместила вызов на удержание.</span><span class="sxs-lookup"><span data-stu-id="82151-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="82151-129">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="82151-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="82151-130">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="82151-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82151-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82151-131">Remarks</span></span>

<span data-ttu-id="82151-132">Не расширяемый.</span><span class="sxs-lookup"><span data-stu-id="82151-132">Not extensible.</span></span> <span data-ttu-id="82151-133">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="82151-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="82151-134">Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API в строке и не использовать эти \_ значения линеконнектедмоде, которые не поддерживаются в согласованной версии.</span><span class="sxs-lookup"><span data-stu-id="82151-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="82151-135">Приложения, не компания cognizant ЛИНЕКОННЕКТЕДМОДЕ, \_ скорее всего предполагают, что вызов, находящиеся в линекаллстате \_ Connected, находится в линеконнектедмоде \_ Active.</span><span class="sxs-lookup"><span data-stu-id="82151-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="82151-136">Неактивные \_ значения линеконнектедмоде Active и линеконнектедмоде \_ используются, когда вызов осуществляется на адресе, который используется совместно с другими станциями (с мостом; см. [**\_ константы линеаддрессшаринг**](lineaddresssharing--constants.md)), в первую очередь на электронные ключевые системы.</span><span class="sxs-lookup"><span data-stu-id="82151-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="82151-137">Если режим подключенного вызова имеет значение "активный", это означает, что вызов подключен на текущей станции (Текущая станция является участником вызова).</span><span class="sxs-lookup"><span data-stu-id="82151-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="82151-138">Если режим вызова имеет состояние "Неактивный", вызов активен на одной или нескольких станциях, но текущая станция не является участником вызова.</span><span class="sxs-lookup"><span data-stu-id="82151-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="82151-139">Если режим вызова равен нулю, приложение должно предположить, что значение — "активно" (это будет ситуация на немостном адресе).</span><span class="sxs-lookup"><span data-stu-id="82151-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="82151-140">Режим может переключаться между активными и неактивными во время вызова, если пользователь присоединяется и оставляет вызов с помощью ручного действия.</span><span class="sxs-lookup"><span data-stu-id="82151-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="82151-141">В такой ситуации с мостом операция [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop) или [**линехолд**](/windows/desktop/api/Tapi/nf-tapi-linehold) может не удалить вызов или поместить его в удержание, так как состояние других станций в вызове может контролироваться (например, при попытке "удержание" вызова, когда участвуют другие станции); Вместо этого вызов можно просто изменить на неактивный режим, если он остается подключенным к другим станциям.</span><span class="sxs-lookup"><span data-stu-id="82151-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="82151-142">Вызов в неактивном состоянии может быть соединен с помощью [**линеансвер**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="82151-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="82151-143">Многие операции, допустимые в вызовах в подключенном состоянии, могут быть невозможными в неактивном режиме, например при мониторинге тонов и цифр, так как станция не участвует в вызове. мониторинг обычно приостанавливается (хотя не отменяется), пока вызов находится в неактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="82151-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="82151-144">Требования</span><span class="sxs-lookup"><span data-stu-id="82151-144">Requirements</span></span>



| <span data-ttu-id="82151-145">Требование</span><span class="sxs-lookup"><span data-stu-id="82151-145">Requirement</span></span> | <span data-ttu-id="82151-146">Значение</span><span class="sxs-lookup"><span data-stu-id="82151-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="82151-147">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="82151-147">TAPI version</span></span><br/> | <span data-ttu-id="82151-148">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="82151-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="82151-149">Header</span><span class="sxs-lookup"><span data-stu-id="82151-149">Header</span></span><br/>       | <dl> <span data-ttu-id="82151-150"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="82151-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82151-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82151-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82151-152">**линеансвер**</span><span class="sxs-lookup"><span data-stu-id="82151-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="82151-153">**линедроп**</span><span class="sxs-lookup"><span data-stu-id="82151-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="82151-154">**линехолд**</span><span class="sxs-lookup"><span data-stu-id="82151-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




