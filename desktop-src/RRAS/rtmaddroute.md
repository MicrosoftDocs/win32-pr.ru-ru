---
title: Функция Ртмаддрауте (RTM. h)
description: Функция Ртмаддрауте добавляет запись маршрута или обновляет существующую запись маршрута.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RAS функции Ртмаддрауте
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672740"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="de7fb-104">Функция Ртмаддрауте</span><span class="sxs-lookup"><span data-stu-id="de7fb-104">RtmAddRoute function</span></span>

<span data-ttu-id="de7fb-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="de7fb-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="de7fb-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="de7fb-107">Функция **ртмаддрауте** добавляет запись маршрута или обновляет существующую запись маршрута.</span><span class="sxs-lookup"><span data-stu-id="de7fb-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="de7fb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de7fb-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="de7fb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="de7fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de7fb-110">*Клиенсандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de7fb-111">Маркер, идентифицирующий клиента, и, следовательно, протокол маршрутизации, который добавил или обновил маршрут.</span><span class="sxs-lookup"><span data-stu-id="de7fb-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="de7fb-112">Получите этот обработчик путем вызова [**ртмрегистерклиент**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="de7fb-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="de7fb-113">*Маршрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de7fb-114">Указатель на структуру, относящуюся к конкретному семейству протоколов, которая указывает новый или обновленный маршрут.</span><span class="sxs-lookup"><span data-stu-id="de7fb-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="de7fb-115">Диспетчер таблиц маршрутизации использует следующие поля для обновления таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="de7fb-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="de7fb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="de7fb-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="de7fb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="de7fb-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="de7fb-118"><dt>**RR, \_ сеть**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="de7fb-119">Указывает номер сети назначения.</span><span class="sxs-lookup"><span data-stu-id="de7fb-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="de7fb-120"><dt>**RR \_ InterfaceID**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="de7fb-121">Указывает индекс интерфейса, через который был получен маршрут.</span><span class="sxs-lookup"><span data-stu-id="de7fb-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="de7fb-122"><dt>**RR \_ некссопаддресс**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="de7fb-123">Указывает адрес маршрутизатора следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="de7fb-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="de7fb-124"><dt>**RR \_ фамилиспеЦификдата**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="de7fb-125">Указывает данные, относящиеся к семейству протоколов.</span><span class="sxs-lookup"><span data-stu-id="de7fb-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="de7fb-126">Хотя данные являются прозрачными для диспетчера таблиц маршрутизации, они рассматриваются при сравнении маршрутов, чтобы определить, изменились ли сведения о маршруте.</span><span class="sxs-lookup"><span data-stu-id="de7fb-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="de7fb-127">Данные также используются для задания значений метрик, которые не зависят от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="de7fb-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="de7fb-128">Следовательно, эти данные используются для определения наилучшего маршрута для целевой сети.</span><span class="sxs-lookup"><span data-stu-id="de7fb-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="de7fb-129"><dt>**RR \_ протоколспеЦификдата**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="de7fb-130">Указывает данные, относящиеся к протоколу маршрутизации, который предоставляет маршрут.</span><span class="sxs-lookup"><span data-stu-id="de7fb-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="de7fb-131"><dt>**\_Метка времени RR**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="de7fb-132">Указывает текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="de7fb-132">Specifies the current system time.</span></span> <span data-ttu-id="de7fb-133">Это поле задается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="de7fb-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="de7fb-134">*TimeToLive* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de7fb-135">Указывает количество секунд, в течение которых указанный маршрут должен храниться в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="de7fb-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="de7fb-136">Если этот параметр имеет значение INFINITE, маршрут сохраняется до тех пор, пока он не будет явно удален.</span><span class="sxs-lookup"><span data-stu-id="de7fb-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="de7fb-137">Текущее ограничение для *TimeToLive* — 2147483 сек (24 + дн.).</span><span class="sxs-lookup"><span data-stu-id="de7fb-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="de7fb-138">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de7fb-139">Указатель на переменную **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="de7fb-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="de7fb-140">Значение этой переменной задается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="de7fb-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="de7fb-141">Значение указывает тип изменения и сведения, возвращенные в предоставленных буферах.</span><span class="sxs-lookup"><span data-stu-id="de7fb-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="de7fb-142">Этот параметр является одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="de7fb-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="de7fb-143">Флаги</span><span class="sxs-lookup"><span data-stu-id="de7fb-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="de7fb-144">Значение</span><span class="sxs-lookup"><span data-stu-id="de7fb-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="de7fb-145"><dt>**RTM — \_ нет \_ изменений**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="de7fb-146">Добавление или обновление либо не изменило какие-либо существенные параметры маршрута, либо запись маршрута не является лучшим маршрутом между записями для целевой сети.</span><span class="sxs-lookup"><span data-stu-id="de7fb-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="de7fb-147"><dt>**\_добавлен маршрут \_ RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="de7fb-148">Маршрут был добавлен для целевой сети.</span><span class="sxs-lookup"><span data-stu-id="de7fb-148">The route was added for the destination network.</span></span> <span data-ttu-id="de7fb-149">Параметр *курбестрауте* указывает на сведения для добавленного маршрута.</span><span class="sxs-lookup"><span data-stu-id="de7fb-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="de7fb-150"><dt>**\_маршрут RTM \_ изменен**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="de7fb-151">По крайней мере один из значимых параметров был изменен для лучшего маршрута к целевой сети.</span><span class="sxs-lookup"><span data-stu-id="de7fb-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="de7fb-152">Значимые параметры:</span><span class="sxs-lookup"><span data-stu-id="de7fb-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="de7fb-153">Идентификатор протокола</span><span class="sxs-lookup"><span data-stu-id="de7fb-153">Protocol identifier</span></span><br/> <span data-ttu-id="de7fb-154">Индекс интерфейса</span><span class="sxs-lookup"><span data-stu-id="de7fb-154">Interface index</span></span><br/> <span data-ttu-id="de7fb-155">Адрес следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="de7fb-155">Next-hop address</span></span><br/> <span data-ttu-id="de7fb-156">Данные, относящиеся к семейству протоколов (включая метрики маршрута)</span><span class="sxs-lookup"><span data-stu-id="de7fb-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="de7fb-157">Параметр *превбестрауте* указывает на сведения о маршруте, которые были перед изменением.</span><span class="sxs-lookup"><span data-stu-id="de7fb-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="de7fb-158">Параметр *курбестрауте* указывает на текущие сведения о маршруте (то есть после изменения).</span><span class="sxs-lookup"><span data-stu-id="de7fb-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="de7fb-159">*Курбестрауте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de7fb-160">Указатель на структуру, которая получает текущие сведения о наилучшем маршруте, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="de7fb-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="de7fb-161">Тип структуры зависит от семейства протоколов, например IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="de7fb-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="de7fb-162">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="de7fb-162">This parameter is optional.</span></span> <span data-ttu-id="de7fb-163">Если вызывающий объект задает для этого параметра **значение NULL** , текущие сведения о наилучшем маршруте не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="de7fb-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="de7fb-164">*Превбестрауте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de7fb-165">Указатель на структуру, которая получает предыдущие сведения о наилучшем маршруте, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="de7fb-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="de7fb-166">Тип структуры зависит от семейства протоколов, например IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="de7fb-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="de7fb-167">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="de7fb-167">This parameter is optional.</span></span> <span data-ttu-id="de7fb-168">Если вызывающий объект задает **значение NULL** для этого параметра, предыдущие сведения о наилучшем маршруте не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="de7fb-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de7fb-169">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de7fb-169">Return value</span></span>

<span data-ttu-id="de7fb-170">Возвращаемое значение является одним из следующих кодов.</span><span class="sxs-lookup"><span data-stu-id="de7fb-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="de7fb-171">Значение</span><span class="sxs-lookup"><span data-stu-id="de7fb-171">Value</span></span>                                                                                                       | <span data-ttu-id="de7fb-172">Описание</span><span class="sxs-lookup"><span data-stu-id="de7fb-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de7fb-173"><dt>**БЕЗ \_ ошибок**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="de7fb-174">Маршрут был успешно добавлен или обновлен.</span><span class="sxs-lookup"><span data-stu-id="de7fb-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="de7fb-175"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="de7fb-176">Параметр "Handle" клиента не является допустимым маркером.</span><span class="sxs-lookup"><span data-stu-id="de7fb-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="de7fb-177"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="de7fb-178">Структура маршрута содержит недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="de7fb-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="de7fb-179"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="de7fb-180">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="de7fb-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="de7fb-181"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="de7fb-182">Недостаточно памяти для выделения записи маршрута.</span><span class="sxs-lookup"><span data-stu-id="de7fb-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="de7fb-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de7fb-183">Remarks</span></span>

<span data-ttu-id="de7fb-184">Функция создает сообщение об изменении маршрута, если в результате этой операции был изменен оптимальный маршрут к целевой сети.</span><span class="sxs-lookup"><span data-stu-id="de7fb-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="de7fb-185">Тем не менее сообщение маршрута-Change не отправляется клиенту, который выполняет этот вызов.</span><span class="sxs-lookup"><span data-stu-id="de7fb-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="de7fb-186">Вместо этого соответствующая информация возвращается этой функцией непосредственно этому клиенту с помощью параметров *flags*, *курбестрауте* и *превбестрауте* .</span><span class="sxs-lookup"><span data-stu-id="de7fb-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="de7fb-187">Требования</span><span class="sxs-lookup"><span data-stu-id="de7fb-187">Requirements</span></span>



| <span data-ttu-id="de7fb-188">Требование</span><span class="sxs-lookup"><span data-stu-id="de7fb-188">Requirement</span></span> | <span data-ttu-id="de7fb-189">Значение</span><span class="sxs-lookup"><span data-stu-id="de7fb-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de7fb-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de7fb-190">Minimum supported client</span></span><br/> | <span data-ttu-id="de7fb-191">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="de7fb-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="de7fb-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de7fb-192">Minimum supported server</span></span><br/> | <span data-ttu-id="de7fb-193">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de7fb-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="de7fb-194">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="de7fb-194">End of server support</span></span><br/>    | <span data-ttu-id="de7fb-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de7fb-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="de7fb-196">Header</span><span class="sxs-lookup"><span data-stu-id="de7fb-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="de7fb-197"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="de7fb-198">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de7fb-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="de7fb-199"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="de7fb-200">DLL</span><span class="sxs-lookup"><span data-stu-id="de7fb-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de7fb-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de7fb-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de7fb-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de7fb-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de7fb-203">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="de7fb-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="de7fb-204">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="de7fb-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="de7fb-205">**ртмделетерауте**</span><span class="sxs-lookup"><span data-stu-id="de7fb-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="de7fb-206">**ртмдекуеуераутечанжемессаже**</span><span class="sxs-lookup"><span data-stu-id="de7fb-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





