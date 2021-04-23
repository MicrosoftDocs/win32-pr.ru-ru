---
title: Функция Ртмкреатинумератионхандле (RTM. h)
description: Функция Ртмкреатинумератионхандле возвращает маркер для использования с Ртменумератежетнекстрауте для просмотра всех маршрутов или подмножества маршрутов, известных диспетчеру таблиц маршрутизации.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RAS функции Ртмкреатинумератионхандле
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135350"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="f834e-104">Функция Ртмкреатинумератионхандле</span><span class="sxs-lookup"><span data-stu-id="f834e-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="f834e-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f834e-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f834e-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="f834e-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f834e-107">Функция **ртмкреатинумератионхандле** возвращает маркер для использования с [**ртменумератежетнекстрауте**](rtmenumerategetnextroute.md) для просмотра всех маршрутов или подмножества маршрутов, известных диспетчеру таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="f834e-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f834e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f834e-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="f834e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f834e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f834e-110">*Протоколфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f834e-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f834e-111">Указывает семейство протоколов для перечислений маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f834e-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="f834e-112">*Енумератионфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f834e-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f834e-113">Указывает, какие маршруты следует перечислить.</span><span class="sxs-lookup"><span data-stu-id="f834e-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="f834e-114">Этот параметр ограничивает набор маршрутов, возвращаемых API перечисления, в подмножество, определенное следующими флагами, и значения в соответствующих элементах структуры, на которые указывает параметр *критериарауте* .</span><span class="sxs-lookup"><span data-stu-id="f834e-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="f834e-115">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="f834e-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f834e-116">енумератионфлагс</span><span class="sxs-lookup"><span data-stu-id="f834e-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="f834e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f834e-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="f834e-118"><dt>**RTM \_ только \_ Эта \_ сеть**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="f834e-119">Перечислите только те маршруты, которые имеют тот же номер сети, что и \_ сетевой член RR структуры, на которую указывает критериарауте.</span><span class="sxs-lookup"><span data-stu-id="f834e-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="f834e-120"><dt>**RTM \_ только \_ этот \_ интерфейс**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="f834e-121">Перечислите только те маршруты, которые были получены через интерфейс, указанный в \_ поле RR InterfaceID структуры, на которую указывает критериарауте.</span><span class="sxs-lookup"><span data-stu-id="f834e-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="f834e-122"><dt>**\_только RTM \_ этот \_ протокол**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="f834e-123">Перечислите только те маршруты, которые были добавлены протоколом маршрутизации, указанным в \_ поле RR раутингпротокол структуры, на которую указывает критериарауте.</span><span class="sxs-lookup"><span data-stu-id="f834e-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="f834e-124"><dt>**\_только \_ лучшие \_ маршруты RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="f834e-125">Перечислите только оптимальные маршруты к каждой из сетей в наборе.</span><span class="sxs-lookup"><span data-stu-id="f834e-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f834e-126">*Критериарауте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f834e-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f834e-127">Указатель на структуру маршрута для конкретного семейства протоколов ([**RTM \_ - \_ маршрут IP**](rtm-ip-route.md) или [**\_ \_ маршрут RTM IPX**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="f834e-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="f834e-128">Значения элементов в этой структуре соответствуют флагам, заданным параметром *енумератионфлагс* .</span><span class="sxs-lookup"><span data-stu-id="f834e-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f834e-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f834e-129">Return value</span></span>

<span data-ttu-id="f834e-130">Если функция выполнена, возвращаемое значение является **маркером** , используемым при последующих вызовах перечисления.</span><span class="sxs-lookup"><span data-stu-id="f834e-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="f834e-131">Если функция завершается с ошибкой или не существует маршрутов с указанными критериями, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f834e-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="f834e-132">Чтобы получить дополнительные сведения, вызовите [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f834e-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="f834e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f834e-133">Value</span></span>                                                                                                       | <span data-ttu-id="f834e-134">Описание</span><span class="sxs-lookup"><span data-stu-id="f834e-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f834e-135"><dt>**ОШИБКИ \_ нет \_ маршрутов**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="f834e-136">Нет маршрутов с указанными критериями.</span><span class="sxs-lookup"><span data-stu-id="f834e-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="f834e-137"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="f834e-138">Один или несколько входных параметров являются недопустимыми (например, неизвестное семейство протоколов, недопустимые флаги перечисления).</span><span class="sxs-lookup"><span data-stu-id="f834e-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="f834e-139"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="f834e-140">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f834e-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="f834e-141"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="f834e-142">Недостаточно памяти для выделения маркера.</span><span class="sxs-lookup"><span data-stu-id="f834e-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="f834e-143">Требования</span><span class="sxs-lookup"><span data-stu-id="f834e-143">Requirements</span></span>



| <span data-ttu-id="f834e-144">Требование</span><span class="sxs-lookup"><span data-stu-id="f834e-144">Requirement</span></span> | <span data-ttu-id="f834e-145">Значение</span><span class="sxs-lookup"><span data-stu-id="f834e-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f834e-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f834e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f834e-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f834e-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="f834e-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f834e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f834e-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f834e-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f834e-150">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f834e-150">End of server support</span></span><br/>    | <span data-ttu-id="f834e-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f834e-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="f834e-152">Header</span><span class="sxs-lookup"><span data-stu-id="f834e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="f834e-153"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="f834e-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f834e-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="f834e-155"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="f834e-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f834e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f834e-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f834e-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f834e-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f834e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f834e-159">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="f834e-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f834e-160">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="f834e-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="f834e-161">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f834e-161">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="f834e-162">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="f834e-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="f834e-163">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="f834e-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="f834e-164">**ртмклосинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="f834e-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="f834e-165">**ртменумератежетнекстрауте**</span><span class="sxs-lookup"><span data-stu-id="f834e-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

