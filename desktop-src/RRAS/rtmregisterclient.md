---
title: Функция Ртмрегистерклиент (RTM. h)
description: Функция Ртмрегистерклиент регистрирует клиента в качестве обработчика указанного протокола. Он устанавливает механизм уведомления об изменении маршрута для клиента и устанавливает параметры протокола.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RAS функции Ртмрегистерклиент
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803484"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="80bf7-105">Функция Ртмрегистерклиент</span><span class="sxs-lookup"><span data-stu-id="80bf7-105">RtmRegisterClient function</span></span>

<span data-ttu-id="80bf7-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="80bf7-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="80bf7-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="80bf7-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="80bf7-108">Функция **ртмрегистерклиент** регистрирует клиента в качестве обработчика указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="80bf7-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="80bf7-109">Он устанавливает механизм уведомления об изменении маршрута для клиента и устанавливает параметры протокола.</span><span class="sxs-lookup"><span data-stu-id="80bf7-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bf7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80bf7-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="80bf7-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="80bf7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80bf7-112">*Протоколфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80bf7-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bf7-113">Указывает семейство протоколов протокола маршрутизации для регистрации.</span><span class="sxs-lookup"><span data-stu-id="80bf7-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="80bf7-114">*Раутингпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80bf7-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bf7-115">Указывает идентификатор протокола маршрутизации, аналогичный тому, который использовался при регистрации в диспетчере маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="80bf7-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="80bf7-116">См. [**регистерпротокол**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span><span class="sxs-lookup"><span data-stu-id="80bf7-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="80bf7-117">*Чанжеевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80bf7-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bf7-118">Указывает, что оптимальный маршрут к сети в таблице изменился.</span><span class="sxs-lookup"><span data-stu-id="80bf7-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="80bf7-119">Диспетчер таблиц маршрутизации сигнализирует об этом событии после изменения лучшего маршрута на любую сеть в таблице.</span><span class="sxs-lookup"><span data-stu-id="80bf7-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="80bf7-120">Дополнительные сведения об уведомлении о смене маршрута см. в разделе [**ртмдекуеуераутечанжемессаже**](rtmdequeueroutechangemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="80bf7-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="80bf7-121">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="80bf7-121">This parameter is optional.</span></span> <span data-ttu-id="80bf7-122">Если вызывающий объект задает для этого параметра **значение NULL** , диспетчер таблиц маршрутизации не уведомляет клиента об изменениях в оптимальном состоянии маршрута.</span><span class="sxs-lookup"><span data-stu-id="80bf7-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="80bf7-123">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80bf7-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80bf7-124">Задает различные параметры для специальной обработки протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="80bf7-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="80bf7-125">В настоящее время поддерживается следующее значение.</span><span class="sxs-lookup"><span data-stu-id="80bf7-125">The following value is currently supported.</span></span>



| <span data-ttu-id="80bf7-126">Флаги</span><span class="sxs-lookup"><span data-stu-id="80bf7-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="80bf7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="80bf7-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="80bf7-128"><dt>**\_ \_ единый маршрут для протокола RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="80bf7-129">Диспетчер таблиц маршрутизации хранит только один маршрут для каждой целевой сети для протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="80bf7-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="80bf7-130">Иными словами, диспетчер таблиц маршрутизации заменяет записи маршрутов с одинаковыми номерами сетей назначения вместо добавления новых.</span><span class="sxs-lookup"><span data-stu-id="80bf7-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80bf7-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80bf7-131">Return value</span></span>

<span data-ttu-id="80bf7-132">При успешном возвращении значение **обработчика** , идентифицирующее клиента при последующих вызовах диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="80bf7-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="80bf7-133">Маркер **null** указывает, что диспетчеру таблиц маршрутизации не удалось зарегистрировать клиент.</span><span class="sxs-lookup"><span data-stu-id="80bf7-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="80bf7-134">Вызовите [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="80bf7-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="80bf7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="80bf7-135">Value</span></span>                                                                                                         | <span data-ttu-id="80bf7-136">Описание</span><span class="sxs-lookup"><span data-stu-id="80bf7-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80bf7-137"><dt>**клиент с ошибкой \_ \_ уже \_ существует**</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="80bf7-138">Другой клиент уже зарегистрирован для работы с указанным Протоколом.</span><span class="sxs-lookup"><span data-stu-id="80bf7-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="80bf7-139"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="80bf7-140">Указанное семейство протоколов не поддерживается, или параметр *flags* является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="80bf7-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="80bf7-141"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="80bf7-142">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="80bf7-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="80bf7-143"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="80bf7-144">Недостаточно памяти для распределения структур данных для клиента.</span><span class="sxs-lookup"><span data-stu-id="80bf7-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="80bf7-145">Требования</span><span class="sxs-lookup"><span data-stu-id="80bf7-145">Requirements</span></span>



| <span data-ttu-id="80bf7-146">Требование</span><span class="sxs-lookup"><span data-stu-id="80bf7-146">Requirement</span></span> | <span data-ttu-id="80bf7-147">Значение</span><span class="sxs-lookup"><span data-stu-id="80bf7-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80bf7-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80bf7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="80bf7-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="80bf7-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="80bf7-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80bf7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="80bf7-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80bf7-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="80bf7-152">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="80bf7-152">End of server support</span></span><br/>    | <span data-ttu-id="80bf7-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80bf7-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="80bf7-154">Header</span><span class="sxs-lookup"><span data-stu-id="80bf7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="80bf7-155"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="80bf7-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80bf7-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="80bf7-157"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="80bf7-158">DLL</span><span class="sxs-lookup"><span data-stu-id="80bf7-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80bf7-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80bf7-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80bf7-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80bf7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bf7-161">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="80bf7-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="80bf7-162">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="80bf7-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="80bf7-163">**Функция**</span><span class="sxs-lookup"><span data-stu-id="80bf7-163">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="80bf7-164">**регистерпротокол**</span><span class="sxs-lookup"><span data-stu-id="80bf7-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="80bf7-165">Идентификаторы семейства протоколов RTMv1</span><span class="sxs-lookup"><span data-stu-id="80bf7-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="80bf7-166">**ртмдекуеуераутечанжемессаже**</span><span class="sxs-lookup"><span data-stu-id="80bf7-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="80bf7-167">**ртмдерегистерклиент**</span><span class="sxs-lookup"><span data-stu-id="80bf7-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 

