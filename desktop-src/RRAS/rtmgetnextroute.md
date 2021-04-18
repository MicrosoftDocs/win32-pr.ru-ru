---
title: Функция Ртмжетнекстрауте (RTM. h)
description: Функция Ртмжетнекстрауте возвращает следующий маршрут из указанного подмножества маршрутов в таблице.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RAS функции Ртмжетнекстрауте
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534475"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="0326b-104">Функция Ртмжетнекстрауте</span><span class="sxs-lookup"><span data-stu-id="0326b-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="0326b-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0326b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="0326b-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="0326b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="0326b-107">Функция **ртмжетнекстрауте** возвращает следующий маршрут из указанного подмножества маршрутов в таблице.</span><span class="sxs-lookup"><span data-stu-id="0326b-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0326b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0326b-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="0326b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0326b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0326b-110">*Протоколфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0326b-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0326b-111">Указывает семейство протоколов для извлекаемых маршрутов, например, IP-адрес или IPX.</span><span class="sxs-lookup"><span data-stu-id="0326b-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="0326b-112">*Енумератионфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0326b-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0326b-113">Указывает, какие маршруты следует перечислить.</span><span class="sxs-lookup"><span data-stu-id="0326b-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="0326b-114">Этот параметр ограничивает набор удаленных маршрутов подмножеством, определенным следующими флагами, и значениями в соответствующих элементах структуры, на которые указывает параметр *критериарауте* .</span><span class="sxs-lookup"><span data-stu-id="0326b-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="0326b-115">Флаги аналогичны параметрам, используемым в [**ртмкреатинумератионхандле**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="0326b-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="0326b-116">*Маршрут* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0326b-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0326b-117">Во входных данных *Маршрутизация* указывает на структуру, относящуюся к конкретному семейству протоколов ( [**RTM \_ - \_ маршруту**](rtm-ip-route.md) или [**\_ \_ маршруту RTM IPX**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="0326b-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="0326b-118">Вызывающая функция предоставляет значения элементов для этой структуры.</span><span class="sxs-lookup"><span data-stu-id="0326b-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="0326b-119">Эти значения в сочетании с параметром *енумератионфлагс* указывают набор, из которого возвращаются маршруты.</span><span class="sxs-lookup"><span data-stu-id="0326b-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="0326b-120">В выходных данных *Маршрутизация* указывает на структуру, которая получает первый маршрут, соответствующий указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="0326b-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0326b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0326b-121">Return value</span></span>

<span data-ttu-id="0326b-122">Если функция выполнена удачно, возвращается значение **No \_ Error**.</span><span class="sxs-lookup"><span data-stu-id="0326b-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="0326b-123">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="0326b-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="0326b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0326b-124">Value</span></span>                                                                                                       | <span data-ttu-id="0326b-125">Описание</span><span class="sxs-lookup"><span data-stu-id="0326b-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0326b-126"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="0326b-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="0326b-127">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="0326b-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="0326b-128"><dt>**ОШИБКИ \_ нет \_ маршрутов**</dt></span><span class="sxs-lookup"><span data-stu-id="0326b-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="0326b-129">Нет маршрутов, соответствующих указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="0326b-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="0326b-130"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="0326b-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="0326b-131">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="0326b-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0326b-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0326b-132">Remarks</span></span>

<span data-ttu-id="0326b-133">Маршруты возвращаются в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="0326b-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="0326b-134">Номер сети</span><span class="sxs-lookup"><span data-stu-id="0326b-134">Network number</span></span>
2.  <span data-ttu-id="0326b-135">Протокол маршрутизации</span><span class="sxs-lookup"><span data-stu-id="0326b-135">Routing protocol</span></span>
3.  <span data-ttu-id="0326b-136">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="0326b-136">Interface identifier</span></span>
4.  <span data-ttu-id="0326b-137">Адрес следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="0326b-137">Next-hop address</span></span>

<span data-ttu-id="0326b-138">Эта функция менее эффективна, чем соответствующие функции обработчика перечисления.</span><span class="sxs-lookup"><span data-stu-id="0326b-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0326b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="0326b-139">Requirements</span></span>



| <span data-ttu-id="0326b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="0326b-140">Requirement</span></span> | <span data-ttu-id="0326b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="0326b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0326b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0326b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0326b-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0326b-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0326b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0326b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0326b-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0326b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0326b-146">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0326b-146">End of server support</span></span><br/>    | <span data-ttu-id="0326b-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0326b-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="0326b-148">Header</span><span class="sxs-lookup"><span data-stu-id="0326b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="0326b-149"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0326b-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="0326b-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0326b-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="0326b-151"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0326b-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="0326b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0326b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0326b-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0326b-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0326b-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0326b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0326b-155">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="0326b-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="0326b-156">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="0326b-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="0326b-157">**ртмклосинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="0326b-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="0326b-158">**ртмкреатинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="0326b-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="0326b-159">**ртменумератежетнекстрауте**</span><span class="sxs-lookup"><span data-stu-id="0326b-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="0326b-160">**ртмжетфирстрауте**</span><span class="sxs-lookup"><span data-stu-id="0326b-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 





