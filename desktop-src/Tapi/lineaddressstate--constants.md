---
description: '\_Константы побитового флага линеаддрессстате описывают различные элементы состояния адреса.'
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Константы LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689397"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="d014c-103">\_Константы линеаддрессстате</span><span class="sxs-lookup"><span data-stu-id="d014c-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="d014c-104">Константы побитового флага **линеаддрессстате \_** описывают различные элементы состояния адреса.</span><span class="sxs-lookup"><span data-stu-id="d014c-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="d014c-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**ЛИНЕАДДРЕСССТАТЕ \_ капсчанже**</span><span class="sxs-lookup"><span data-stu-id="d014c-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-106">Указывает, что из-за изменений, внесенных в конфигурацию пользователем или в других обстоятельствах, изменился один или несколько элементов структуры [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) для адреса.</span><span class="sxs-lookup"><span data-stu-id="d014c-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="d014c-107">Приложение должно использовать [**линежетаддресскапс**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) для чтения обновленной структуры.</span><span class="sxs-lookup"><span data-stu-id="d014c-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="d014c-108">Если поставщик услуг отправляет сообщение [**Line \_ аддрессстате**](line-addressstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, получают [**строки \_ ЛИНЕДЕВСТАТЕ**](line-linedevstate.md) сообщения, указывающие линедевстате \_ reinit, что требует от них завершения работы и повторной инициализации подключения к TAPI для получения обновленной информации.</span><span class="sxs-lookup"><span data-stu-id="d014c-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**ЛИНЕАДДРЕСССТАТЕ \_ девспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="d014c-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-110">Изменился элемент состояния адреса, относящийся к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="d014c-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**ЛИНЕАДДРЕСССТАТЕ \_ вперед**</span><span class="sxs-lookup"><span data-stu-id="d014c-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-112">Состояние пересылки адреса изменилось, включая, возможно, число колец для определения условия "без ответа".</span><span class="sxs-lookup"><span data-stu-id="d014c-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="d014c-113">Приложение должно проверить состояние адреса, чтобы определить сведения о текущем состоянии пересылки адреса.</span><span class="sxs-lookup"><span data-stu-id="d014c-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**ЛИНЕАДДРЕСССТАТЕ \_ инусемани**</span><span class="sxs-lookup"><span data-stu-id="d014c-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-115">Отслеживаемый или переданный мостский адрес был изменен с помощью одной станции, чтобы она использовалась несколькими станциями.</span><span class="sxs-lookup"><span data-stu-id="d014c-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**ЛИНЕАДДРЕСССТАТЕ \_ инусеоне**</span><span class="sxs-lookup"><span data-stu-id="d014c-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-117">Адрес изменен с режима простоя или используется многими станциями, которые используют мост для использования только одной станцией.</span><span class="sxs-lookup"><span data-stu-id="d014c-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**ЛИНЕАДДРЕСССТАТЕ \_ инусезеро**</span><span class="sxs-lookup"><span data-stu-id="d014c-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-119">Адрес был изменен на бездействие (он не используется ни одной из станций).</span><span class="sxs-lookup"><span data-stu-id="d014c-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**ЛИНЕАДДРЕСССТАТЕ \_ нумкаллс**</span><span class="sxs-lookup"><span data-stu-id="d014c-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-121">Число вызовов в адресе изменилось.</span><span class="sxs-lookup"><span data-stu-id="d014c-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="d014c-122">Это результат таких событий, как новый входящий вызов, исходящий вызов по адресу или вызов, изменяющий состояние его удержания.</span><span class="sxs-lookup"><span data-stu-id="d014c-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="d014c-123">Этот флаг охватывает изменения в любом из членов **двнумактивекаллс**, **двнумонхолдкаллс** и **двнумонхолдпендингкаллс** в структуре [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="d014c-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="d014c-124">Приложение должно проверить все три из этих членов при получении сообщения [**Line \_ аддрессстате**](line-addressstate.md) (нумкаллс).</span><span class="sxs-lookup"><span data-stu-id="d014c-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**ЛИНЕАДДРЕСССТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="d014c-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-126">Address — изменились элементы состояния, отличные от перечисленных ниже.</span><span class="sxs-lookup"><span data-stu-id="d014c-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="d014c-127">Приложение должно проверить состояние текущего адреса, чтобы определить, какие элементы были изменены.</span><span class="sxs-lookup"><span data-stu-id="d014c-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d014c-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**ЛИНЕАДДРЕСССТАТЕ \_ терминалов**</span><span class="sxs-lookup"><span data-stu-id="d014c-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d014c-129">Параметры терминала для адреса были изменены.</span><span class="sxs-lookup"><span data-stu-id="d014c-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d014c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d014c-130">Remarks</span></span>

<span data-ttu-id="d014c-131">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="d014c-131">No extensibility.</span></span> <span data-ttu-id="d014c-132">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="d014c-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="d014c-133">Приложение получает уведомление об изменениях этих элементов состояния в [**строке сообщения \_ аддрессстате**](line-addressstate.md) .</span><span class="sxs-lookup"><span data-stu-id="d014c-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="d014c-134">Возможности устройства для адресации указывают на то, какие изменения состояния адресов могут быть переданы по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="d014c-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="d014c-135">Требования</span><span class="sxs-lookup"><span data-stu-id="d014c-135">Requirements</span></span>



| <span data-ttu-id="d014c-136">Требование</span><span class="sxs-lookup"><span data-stu-id="d014c-136">Requirement</span></span> | <span data-ttu-id="d014c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d014c-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d014c-138">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d014c-138">TAPI version</span></span><br/> | <span data-ttu-id="d014c-139">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d014c-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d014c-140">Header</span><span class="sxs-lookup"><span data-stu-id="d014c-140">Header</span></span><br/>       | <dl> <span data-ttu-id="d014c-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d014c-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d014c-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d014c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d014c-143">**Строка \_ аддрессстате**</span><span class="sxs-lookup"><span data-stu-id="d014c-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="d014c-144">**Строка \_ линедевстате**</span><span class="sxs-lookup"><span data-stu-id="d014c-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="d014c-145">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="d014c-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="d014c-146">**линеаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="d014c-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="d014c-147">**линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="d014c-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




