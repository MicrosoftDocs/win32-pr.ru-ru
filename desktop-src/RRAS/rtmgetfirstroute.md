---
title: Функция Ртмжетфирстрауте (RTM. h)
description: Функция Ртмжетфирстрауте возвращает первый маршрут из указанного подмножества маршрутов в таблице.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- RAS функции Ртмжетфирстрауте
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136370"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="d48c1-104">Функция Ртмжетфирстрауте</span><span class="sxs-lookup"><span data-stu-id="d48c1-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="d48c1-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d48c1-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d48c1-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="d48c1-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="d48c1-107">Функция **ртмжетфирстрауте** возвращает первый маршрут из указанного подмножества маршрутов в таблице.</span><span class="sxs-lookup"><span data-stu-id="d48c1-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d48c1-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="d48c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d48c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48c1-110">*Протоколфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d48c1-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c1-111">Указывает семейство протоколов для извлекаемых маршрутов, например, IP-адрес или IPX.</span><span class="sxs-lookup"><span data-stu-id="d48c1-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="d48c1-112">*Енумератионфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d48c1-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c1-113">Указывает, ограничивает набор удаленных маршрутов подмножеством, определенным этими флагами, и значениями соответствующих элементов структуры, на которые указывает параметр *критериарауте* .</span><span class="sxs-lookup"><span data-stu-id="d48c1-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="d48c1-114">Флаги аналогичны параметрам, используемым в [**ртмкреатинумератионхандле**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="d48c1-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48c1-115">*Маршрут* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d48c1-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d48c1-116">Во входных данных *Маршрутизация* указывает на структуру, относящуюся к конкретному семейству протоколов ( [**RTM \_ - \_ маршруту**](rtm-ip-route.md) или [**\_ \_ маршруту RTM IPX**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="d48c1-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="d48c1-117">Вызывающая функция предоставляет значения элементов для этой структуры.</span><span class="sxs-lookup"><span data-stu-id="d48c1-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="d48c1-118">Эти значения в сочетании с параметром *енумератионфлагс* указывают набор, из которого возвращаются маршруты.</span><span class="sxs-lookup"><span data-stu-id="d48c1-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="d48c1-119">Выходные данные out, *Маршрутизация* указывает на первый маршрут, соответствующий указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="d48c1-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48c1-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d48c1-120">Return value</span></span>

<span data-ttu-id="d48c1-121">Если функция выполнена удачно, возвращается значение NO \_ Error.</span><span class="sxs-lookup"><span data-stu-id="d48c1-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="d48c1-122">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="d48c1-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="d48c1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d48c1-123">Value</span></span>                                                                                                       | <span data-ttu-id="d48c1-124">Описание</span><span class="sxs-lookup"><span data-stu-id="d48c1-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d48c1-125"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="d48c1-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="d48c1-126">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="d48c1-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="d48c1-127"><dt>**ОШИБКИ \_ нет \_ маршрутов**</dt></span><span class="sxs-lookup"><span data-stu-id="d48c1-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="d48c1-128">Нет маршрутов, соответствующих указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="d48c1-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="d48c1-129"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="d48c1-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="d48c1-130">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="d48c1-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d48c1-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d48c1-131">Remarks</span></span>

<span data-ttu-id="d48c1-132">Маршруты возвращаются в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d48c1-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="d48c1-133">Номер сети</span><span class="sxs-lookup"><span data-stu-id="d48c1-133">Network number</span></span>
2.  <span data-ttu-id="d48c1-134">Протокол маршрутизации</span><span class="sxs-lookup"><span data-stu-id="d48c1-134">Routing protocol</span></span>
3.  <span data-ttu-id="d48c1-135">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="d48c1-135">Interface identifier</span></span>
4.  <span data-ttu-id="d48c1-136">Адрес следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="d48c1-136">Next-hop address</span></span>

<span data-ttu-id="d48c1-137">Эта функция менее эффективна, чем соответствующая функция-обработчик перечисления, [**ртменумератежетнекстрауте**](rtmenumerategetnextroute.md).</span><span class="sxs-lookup"><span data-stu-id="d48c1-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d48c1-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d48c1-138">Requirements</span></span>



| <span data-ttu-id="d48c1-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d48c1-139">Requirement</span></span> | <span data-ttu-id="d48c1-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d48c1-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d48c1-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d48c1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d48c1-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d48c1-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d48c1-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d48c1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d48c1-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d48c1-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d48c1-145">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d48c1-145">End of server support</span></span><br/>    | <span data-ttu-id="d48c1-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d48c1-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="d48c1-147">Header</span><span class="sxs-lookup"><span data-stu-id="d48c1-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d48c1-148"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d48c1-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="d48c1-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d48c1-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="d48c1-150"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d48c1-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="d48c1-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d48c1-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48c1-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48c1-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48c1-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d48c1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48c1-154">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="d48c1-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="d48c1-155">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="d48c1-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="d48c1-156">**ртмклосинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="d48c1-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="d48c1-157">**ртмкреатинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="d48c1-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="d48c1-158">**ртменумератежетнекстрауте**</span><span class="sxs-lookup"><span data-stu-id="d48c1-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="d48c1-159">**ртмжетнекстрауте**</span><span class="sxs-lookup"><span data-stu-id="d48c1-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 





