---
title: Функция Ртмдекуеуераутечанжемессаже (RTM. h)
description: Функция Ртмдекуеуераутечанжемессаже возвращает следующее сообщение маршрута-Change в очереди, связанной с указанным клиентом.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RAS функции Ртмдекуеуераутечанжемессаже
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136371"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="ea560-104">Функция Ртмдекуеуераутечанжемессаже</span><span class="sxs-lookup"><span data-stu-id="ea560-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="ea560-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ea560-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="ea560-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="ea560-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="ea560-107">Функция **ртмдекуеуераутечанжемессаже** возвращает следующее сообщение маршрута-Change в очереди, связанной с указанным клиентом.</span><span class="sxs-lookup"><span data-stu-id="ea560-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea560-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea560-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="ea560-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea560-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea560-110">*Клиенсандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea560-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea560-111">Обработчик, идентифицирующий клиента, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="ea560-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="ea560-112">Получите этот обработчик путем вызова [**ртмрегистерклиент**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="ea560-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea560-113">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea560-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea560-114">Указатель на переменную **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ea560-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="ea560-115">Значение этой переменной задается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ea560-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="ea560-116">Значение указывает тип сообщения об изменении и сведения, возвращенные в предоставленных буферах.</span><span class="sxs-lookup"><span data-stu-id="ea560-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="ea560-117">Этот параметр является одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="ea560-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="ea560-118">Флаги</span><span class="sxs-lookup"><span data-stu-id="ea560-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="ea560-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ea560-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="ea560-120"><dt>**\_добавлен маршрут \_ RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="ea560-121">Первый маршрут был добавлен для определенной конечной сети.</span><span class="sxs-lookup"><span data-stu-id="ea560-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="ea560-122">Параметр *курбестрауте* указывает на сведения для добавленного маршрута.</span><span class="sxs-lookup"><span data-stu-id="ea560-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="ea560-123"><dt>**\_маршрут RTM \_ удален**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="ea560-124">Был удален только один маршрут, доступный для конкретной конечной сети.</span><span class="sxs-lookup"><span data-stu-id="ea560-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="ea560-125">Параметр *превбестрауте* указывает на сведения об удаленном маршруте.</span><span class="sxs-lookup"><span data-stu-id="ea560-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="ea560-126"><dt>**\_маршрут RTM \_ изменен**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="ea560-127">По крайней мере один из значимых параметров был изменен для лучшего маршрута к определенной конечной сети.</span><span class="sxs-lookup"><span data-stu-id="ea560-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="ea560-128">Значимые параметры:</span><span class="sxs-lookup"><span data-stu-id="ea560-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="ea560-129">Идентификатор протокола</span><span class="sxs-lookup"><span data-stu-id="ea560-129">Protocol identifier</span></span><br/> <span data-ttu-id="ea560-130">Индекс интерфейса</span><span class="sxs-lookup"><span data-stu-id="ea560-130">Interface index</span></span><br/> <span data-ttu-id="ea560-131">Адрес следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="ea560-131">Next-hop address</span></span><br/> <span data-ttu-id="ea560-132">Данные, относящиеся к семейству протоколов (включая метрики маршрута)</span><span class="sxs-lookup"><span data-stu-id="ea560-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="ea560-133">Параметр *превбестрауте* указывает на сведения о маршруте, которые были перед изменением.</span><span class="sxs-lookup"><span data-stu-id="ea560-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="ea560-134">Параметр *курбестрауте* указывает на текущие сведения о маршруте (то есть после изменения).</span><span class="sxs-lookup"><span data-stu-id="ea560-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="ea560-135">*Курбестрауте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea560-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea560-136">Указатель на структуру, которая получает текущие сведения о наилучшем маршруте (если они есть).</span><span class="sxs-lookup"><span data-stu-id="ea560-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="ea560-137">Тип структуры зависит от семейства протоколов, например IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="ea560-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="ea560-138">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ea560-138">This parameter is optional.</span></span> <span data-ttu-id="ea560-139">Если вызывающий объект задает для этого параметра **значение NULL** , текущие сведения о наилучшем маршруте не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="ea560-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="ea560-140">*Превбестрауте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea560-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea560-141">Указатель на структуру, которая получает предыдущие сведения о наилучшем маршруте, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="ea560-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="ea560-142">Тип структуры зависит от семейства протоколов, например IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="ea560-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="ea560-143">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ea560-143">This parameter is optional.</span></span> <span data-ttu-id="ea560-144">Если вызывающий объект задает для этого параметра **значение NULL** , то предыдущая информация о наилучшем маршруте не возвращается.</span><span class="sxs-lookup"><span data-stu-id="ea560-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea560-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea560-145">Return value</span></span>

<span data-ttu-id="ea560-146">Возвращаемое значение является одним из следующих кодов.</span><span class="sxs-lookup"><span data-stu-id="ea560-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="ea560-147">Значение</span><span class="sxs-lookup"><span data-stu-id="ea560-147">Value</span></span>                                                                                                       | <span data-ttu-id="ea560-148">Описание</span><span class="sxs-lookup"><span data-stu-id="ea560-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea560-149"><dt>**БЕЗ \_ ошибок**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="ea560-150">Это сообщение было последним сообщением в очереди клиента.</span><span class="sxs-lookup"><span data-stu-id="ea560-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="ea560-151">Объект события сброшен.</span><span class="sxs-lookup"><span data-stu-id="ea560-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="ea560-152"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="ea560-153">Параметр *клиенсандле* не является допустимым маркером или при регистрации клиент не предоставил объект события для уведомления об изменении сообщения (см. [**ртмрегистерклиент**](rtmregisterclient.md)).</span><span class="sxs-lookup"><span data-stu-id="ea560-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="ea560-154"><dt>**Ошибка при \_ дополнительных \_ сообщениях**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="ea560-155">Очередь клиента содержит дополнительные сообщения.</span><span class="sxs-lookup"><span data-stu-id="ea560-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="ea560-156">Чтобы разрешить диспетчеру таблиц маршрутизации освобождать ресурсы, связанные с ожидающими сообщениями, клиент должен вызвать **ртмдекуеуераутечанжемессаже** снова как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="ea560-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="ea560-157"><dt>**сообщения об ОШИБКАх \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="ea560-158">Очередь клиента не содержит сообщений; вызов был незапрошен.</span><span class="sxs-lookup"><span data-stu-id="ea560-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="ea560-159">Событие сброшено.</span><span class="sxs-lookup"><span data-stu-id="ea560-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="ea560-160"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="ea560-161">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ea560-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="ea560-162">Требования</span><span class="sxs-lookup"><span data-stu-id="ea560-162">Requirements</span></span>



| <span data-ttu-id="ea560-163">Требование</span><span class="sxs-lookup"><span data-stu-id="ea560-163">Requirement</span></span> | <span data-ttu-id="ea560-164">Значение</span><span class="sxs-lookup"><span data-stu-id="ea560-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea560-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea560-165">Minimum supported client</span></span><br/> | <span data-ttu-id="ea560-166">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ea560-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ea560-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea560-167">Minimum supported server</span></span><br/> | <span data-ttu-id="ea560-168">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ea560-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea560-169">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ea560-169">End of server support</span></span><br/>    | <span data-ttu-id="ea560-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea560-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="ea560-171">Header</span><span class="sxs-lookup"><span data-stu-id="ea560-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea560-172"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea560-173">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ea560-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea560-174"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea560-175">DLL</span><span class="sxs-lookup"><span data-stu-id="ea560-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea560-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea560-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea560-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea560-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea560-178">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="ea560-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="ea560-179">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="ea560-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="ea560-180">**ртмрегистерклиент**</span><span class="sxs-lookup"><span data-stu-id="ea560-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





