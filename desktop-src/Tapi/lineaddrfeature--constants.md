---
description: В \_ константах линеаддрфеатуре перечислены операции, которые могут быть вызваны по адресу.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Константы LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675541"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="fd038-103">\_Константы линеаддрфеатуре</span><span class="sxs-lookup"><span data-stu-id="fd038-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="fd038-104">В константах **линеаддрфеатуре \_** перечислены операции, которые могут быть вызваны по адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="fd038-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**ЛИНЕАДДРФЕАТУРЕ \_ вперед**</span><span class="sxs-lookup"><span data-stu-id="fd038-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-106">Адрес можно перенаправить.</span><span class="sxs-lookup"><span data-stu-id="fd038-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**ЛИНЕАДДРФЕАТУРЕ \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="fd038-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-108">Исходящий вызов может быть размещен по адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**\_Отправка линеаддрфеатуре**</span><span class="sxs-lookup"><span data-stu-id="fd038-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-110">Вызов можно получить по адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккупдирект**</span><span class="sxs-lookup"><span data-stu-id="fd038-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-112">Функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно использовать для получения вызова по определенному адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккупграуп**</span><span class="sxs-lookup"><span data-stu-id="fd038-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-114">Функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно использовать для выбора вызова в группе.</span><span class="sxs-lookup"><span data-stu-id="fd038-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккуфелд**</span><span class="sxs-lookup"><span data-stu-id="fd038-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-116">Функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (с адресом назначения **null** ) можно использовать для получения вызова, который хранится по адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="fd038-117">Обычно это используется только в расположении, исключающем мост.</span><span class="sxs-lookup"><span data-stu-id="fd038-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**ЛИНЕАДДРФЕАТУРЕ \_ пиккупваитинг**</span><span class="sxs-lookup"><span data-stu-id="fd038-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-119">Чтобы получить ожидающий вызов, можно использовать функцию [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (с адресом назначения **null** ).</span><span class="sxs-lookup"><span data-stu-id="fd038-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="fd038-120">Обратите внимание, что это не обязательно указывает на фактическое присутствие ожидающего вызова, поскольку для устройства телефонии часто бывает невозможно автоматически обнаружить такой вызов. Однако он указывает, что функция-ловушка будет вызываться для попытки переключения на такой вызов.</span><span class="sxs-lookup"><span data-stu-id="fd038-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**ЛИНЕАДДРФЕАТУРЕ \_ сетмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="fd038-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-122">Для этого адреса можно задать элемент управления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fd038-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**ЛИНЕАДДРФЕАТУРЕ \_ сеттерминал**</span><span class="sxs-lookup"><span data-stu-id="fd038-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-124">Можно задать режимы терминала для этого адреса.</span><span class="sxs-lookup"><span data-stu-id="fd038-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**ЛИНЕАДДРФЕАТУРЕ \_ сетупконф**</span><span class="sxs-lookup"><span data-stu-id="fd038-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-126">В этом адресе можно настроить конференц-вызов с **нулевым** начальным вызовом.</span><span class="sxs-lookup"><span data-stu-id="fd038-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**ЛИНЕАДДРФЕАТУРЕ \_ ункомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="fd038-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-128">Запросы на завершение вызовов могут быть отменены по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**\_НЕприпаркованный линеаддрфеатуре**</span><span class="sxs-lookup"><span data-stu-id="fd038-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-130">Вызовы можно отменять с помощью этого адреса.</span><span class="sxs-lookup"><span data-stu-id="fd038-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="fd038-131">Если в элементе **дваддрессфеатурес** в [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) не задано ни одного нового измененного бита "раскладки", но \_ установлен бит раскладки линеаддрфеатуре, то любой из режимов подбора может работать; поставщик услуг просто не указал, какие из них.</span><span class="sxs-lookup"><span data-stu-id="fd038-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**ЛИНЕАДДРФЕАТУРЕ \_ форвардднд**</span><span class="sxs-lookup"><span data-stu-id="fd038-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-133">Функция [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (с пустым адресом назначения) может использоваться для включения функции "не беспокоить" в адресе.</span><span class="sxs-lookup"><span data-stu-id="fd038-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="fd038-134">\_Также будет задано перенаправление линеаддрфеатуре.</span><span class="sxs-lookup"><span data-stu-id="fd038-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd038-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**ЛИНЕАДДРФЕАТУРЕ \_ форвардфвд**</span><span class="sxs-lookup"><span data-stu-id="fd038-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fd038-136">Функцию [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) можно использовать для переадресации вызовов по адресу на другие числа.</span><span class="sxs-lookup"><span data-stu-id="fd038-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="fd038-137">\_Также будет задано перенаправление линеаддрфеатуре.</span><span class="sxs-lookup"><span data-stu-id="fd038-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="fd038-138">Если в элементе **дваддрессфеатурес** в [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) не задан ни один из новых измененных бит пересылки, но установлен бит перенаправления линеаддрфеатуре \_ , то любой из режимов прямого доступа может работать; поставщик услуг просто не указал, какие из них.</span><span class="sxs-lookup"><span data-stu-id="fd038-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd038-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd038-139">Remarks</span></span>

<span data-ttu-id="fd038-140">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="fd038-140">No extensibility.</span></span> <span data-ttu-id="fd038-141">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="fd038-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="fd038-142">Эта константа используется в [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (возвращается [**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) и в [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (возвращается [**линежетаддрессстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span><span class="sxs-lookup"><span data-stu-id="fd038-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="fd038-143">**Линеаддресскапс** сообщает о доступности компонентов адреса поставщиком услуг (в основном коммутаторе) для заданного адреса.</span><span class="sxs-lookup"><span data-stu-id="fd038-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="fd038-144">Приложение сделает это определение при инициализации.</span><span class="sxs-lookup"><span data-stu-id="fd038-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="fd038-145">Структура [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) сообщает об определенном адресе, который может вызывать функции, пока адрес находится в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="fd038-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="fd038-146">Приложение сделает это определение динамически после изменения состояния адреса, как правило, вызванные действиями, связанными с вызовами по адресу.</span><span class="sxs-lookup"><span data-stu-id="fd038-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd038-147">Требования</span><span class="sxs-lookup"><span data-stu-id="fd038-147">Requirements</span></span>



| <span data-ttu-id="fd038-148">Требование</span><span class="sxs-lookup"><span data-stu-id="fd038-148">Requirement</span></span> | <span data-ttu-id="fd038-149">Значение</span><span class="sxs-lookup"><span data-stu-id="fd038-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fd038-150">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="fd038-150">TAPI version</span></span><br/> | <span data-ttu-id="fd038-151">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fd038-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fd038-152">Header</span><span class="sxs-lookup"><span data-stu-id="fd038-152">Header</span></span><br/>       | <dl> <span data-ttu-id="fd038-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd038-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd038-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd038-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd038-155">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="fd038-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="fd038-156">**линеаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="fd038-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="fd038-157">**линефорвард**</span><span class="sxs-lookup"><span data-stu-id="fd038-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="fd038-158">**линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="fd038-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="fd038-159">**линежетаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="fd038-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="fd038-160">**линепиккуп**</span><span class="sxs-lookup"><span data-stu-id="fd038-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




