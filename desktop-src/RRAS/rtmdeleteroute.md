---
title: Функция Ртмделетерауте (RTM. h)
description: Функция Ртмделетерауте удаляет запись маршрута.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RAS функции Ртмделетерауте
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988881"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="dda6b-104">Функция Ртмделетерауте</span><span class="sxs-lookup"><span data-stu-id="dda6b-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="dda6b-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dda6b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="dda6b-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="dda6b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="dda6b-107">Функция **ртмделетерауте** удаляет запись маршрута.</span><span class="sxs-lookup"><span data-stu-id="dda6b-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda6b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dda6b-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="dda6b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dda6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda6b-110">*Клиенсандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dda6b-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dda6b-111">Маркер, идентифицирующий клиента и, следовательно, протокол маршрутизации добавленного или обновленного маршрута.</span><span class="sxs-lookup"><span data-stu-id="dda6b-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="dda6b-112">Получите этот обработчик путем вызова [**ртмрегистерклиент**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="dda6b-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="dda6b-113">*Маршрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dda6b-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dda6b-114">Указатель на структуру, относящуюся к конкретному семейству протоколов, которая указывает новый или обновленный маршрут.</span><span class="sxs-lookup"><span data-stu-id="dda6b-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="dda6b-115">Диспетчер таблиц маршрутизации использует следующие поля для обновления таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dda6b-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="dda6b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dda6b-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="dda6b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dda6b-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="dda6b-118"><dt>**RR, \_ сеть**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="dda6b-119">Указывает номер сети назначения.</span><span class="sxs-lookup"><span data-stu-id="dda6b-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="dda6b-120"><dt>**RR \_ InterfaceID**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="dda6b-121">Указывает индекс интерфейса, через который был получен маршрут.</span><span class="sxs-lookup"><span data-stu-id="dda6b-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="dda6b-122"><dt>**RR \_ некссопаддресс**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="dda6b-123">Указывает сетевой адрес маршрутизатора следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="dda6b-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="dda6b-124">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dda6b-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dda6b-125">Указатель на набор флагов, указывающих тип сообщения об изменении, и сведения, которые были помещены в предоставленные буферы.</span><span class="sxs-lookup"><span data-stu-id="dda6b-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="dda6b-126">Этот параметр может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dda6b-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="dda6b-127">Флаги</span><span class="sxs-lookup"><span data-stu-id="dda6b-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="dda6b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dda6b-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="dda6b-129"><dt>**RTM — \_ нет \_ изменений**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="dda6b-130">Удаление маршрута не повлияло на оптимальный маршрут к любой целевой сети.</span><span class="sxs-lookup"><span data-stu-id="dda6b-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="dda6b-131">Другими словами, другая запись представляет маршрут к той же конечной сети и имеет более низкую метрику.</span><span class="sxs-lookup"><span data-stu-id="dda6b-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="dda6b-132"><dt>**\_маршрут RTM \_ удален**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="dda6b-133">Удаленный маршрут был единственным доступным для конкретной целевой сети.</span><span class="sxs-lookup"><span data-stu-id="dda6b-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="dda6b-134"><dt>**\_маршрут RTM \_ изменен**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="dda6b-135">После удаления этого маршрута лучше подходит другой маршрут к определенной конечной сети.</span><span class="sxs-lookup"><span data-stu-id="dda6b-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="dda6b-136">*Курбестрауте* указывает на сведения о новом оптимальном маршруте.</span><span class="sxs-lookup"><span data-stu-id="dda6b-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="dda6b-137">*Курбестрауте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dda6b-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dda6b-138">Указатель на структуру, которая получает текущие сведения о наилучшем маршруте, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="dda6b-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="dda6b-139">Тип структуры зависит от семейства протоколов, например IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="dda6b-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="dda6b-140">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="dda6b-140">This parameter is optional.</span></span> <span data-ttu-id="dda6b-141">Если вызывающий объект задает для этого параметра **значение NULL** , текущие сведения о наилучшем маршруте не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="dda6b-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda6b-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dda6b-142">Return value</span></span>

<span data-ttu-id="dda6b-143">Если функция выполнена удачно, возвращается значение **No \_ Error**.</span><span class="sxs-lookup"><span data-stu-id="dda6b-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="dda6b-144">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="dda6b-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="dda6b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="dda6b-145">Value</span></span>                                                                                                       | <span data-ttu-id="dda6b-146">Описание</span><span class="sxs-lookup"><span data-stu-id="dda6b-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dda6b-147"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="dda6b-148">Параметр "Handle" клиента не является допустимым маркером.</span><span class="sxs-lookup"><span data-stu-id="dda6b-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="dda6b-149"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="dda6b-150">Структура маршрута, на которую указывает параметр *Route* , содержит значение элемента.</span><span class="sxs-lookup"><span data-stu-id="dda6b-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="dda6b-151"><dt>**Ошибка \_ без \_ такого \_ маршрута**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="dda6b-152">В таблице маршрутизации нет записей, соответствующих параметрам указанного маршрута.</span><span class="sxs-lookup"><span data-stu-id="dda6b-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="dda6b-153"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="dda6b-154">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="dda6b-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="dda6b-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dda6b-155">Remarks</span></span>

<span data-ttu-id="dda6b-156">Функция создает сообщение об изменении маршрута, если оптимальный маршрут к целевой сети изменился в результате удаления.</span><span class="sxs-lookup"><span data-stu-id="dda6b-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="dda6b-157">Тем не менее сообщение маршрута-Change не отправляется клиенту, который выполняет этот вызов.</span><span class="sxs-lookup"><span data-stu-id="dda6b-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="dda6b-158">Вместо этого соответствующая информация возвращается этой функцией непосредственно этому клиенту.</span><span class="sxs-lookup"><span data-stu-id="dda6b-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda6b-159">Требования</span><span class="sxs-lookup"><span data-stu-id="dda6b-159">Requirements</span></span>



| <span data-ttu-id="dda6b-160">Требование</span><span class="sxs-lookup"><span data-stu-id="dda6b-160">Requirement</span></span> | <span data-ttu-id="dda6b-161">Значение</span><span class="sxs-lookup"><span data-stu-id="dda6b-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dda6b-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dda6b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="dda6b-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dda6b-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="dda6b-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dda6b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="dda6b-165">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dda6b-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dda6b-166">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dda6b-166">End of server support</span></span><br/>    | <span data-ttu-id="dda6b-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dda6b-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="dda6b-168">Header</span><span class="sxs-lookup"><span data-stu-id="dda6b-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="dda6b-169"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="dda6b-170">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dda6b-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="dda6b-171"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="dda6b-172">DLL</span><span class="sxs-lookup"><span data-stu-id="dda6b-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dda6b-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dda6b-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda6b-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dda6b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda6b-175">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="dda6b-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="dda6b-176">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="dda6b-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="dda6b-177">**ртмаддрауте**</span><span class="sxs-lookup"><span data-stu-id="dda6b-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="dda6b-178">**ртмдекуеуераутечанжемессаже**</span><span class="sxs-lookup"><span data-stu-id="dda6b-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





