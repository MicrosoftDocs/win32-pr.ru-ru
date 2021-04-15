---
title: Функция Ртмисрауте (RTM. h)
description: Функция Ртмисрауте определяет, существует ли один или несколько маршрутов к указанной целевой сети. Если это так, функция возвращает сведения для лучшего маршрута к этой сети.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RAS функции Ртмисрауте
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492114"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="488ef-105">Функция Ртмисрауте</span><span class="sxs-lookup"><span data-stu-id="488ef-105">RtmIsRoute function</span></span>

<span data-ttu-id="488ef-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="488ef-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="488ef-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="488ef-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="488ef-108">Функция **ртмисрауте** определяет, существует ли один или несколько маршрутов к указанной целевой сети.</span><span class="sxs-lookup"><span data-stu-id="488ef-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="488ef-109">Если это так, функция возвращает сведения для лучшего маршрута к этой сети.</span><span class="sxs-lookup"><span data-stu-id="488ef-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="488ef-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="488ef-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="488ef-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="488ef-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488ef-112">*Протоколфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="488ef-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="488ef-113">Указывает тип структуры данных, на которую указывает *сетевой* параметр, например, [**IP- \_ сеть**](ip-network.md), [**IPX \_**](ipx-network.md).</span><span class="sxs-lookup"><span data-stu-id="488ef-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="488ef-114">*Сеть* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="488ef-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="488ef-115">Указатель на структуру, указывающую номер сети для конкретного семейства протоколов.</span><span class="sxs-lookup"><span data-stu-id="488ef-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="488ef-116">Эти данные идентифицируют сеть, для которой вызывающий объект ищет сведения о маршруте.</span><span class="sxs-lookup"><span data-stu-id="488ef-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="488ef-117">*Бестрауте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="488ef-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="488ef-118">Указатель на структуру, относящуюся к конкретному семейству протоколов, которая получает текущие наиболее подходящие сведения о маршруте, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="488ef-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="488ef-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="488ef-119">Return value</span></span>

<span data-ttu-id="488ef-120">Возвращаемое значение является одним из следующих кодов.</span><span class="sxs-lookup"><span data-stu-id="488ef-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="488ef-121">Значение</span><span class="sxs-lookup"><span data-stu-id="488ef-121">Value</span></span>                                                                                                       | <span data-ttu-id="488ef-122">Описание</span><span class="sxs-lookup"><span data-stu-id="488ef-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="488ef-123"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="488ef-124">Существует по крайней мере один маршрут к указанной сети.</span><span class="sxs-lookup"><span data-stu-id="488ef-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="488ef-125">Лучший маршрут возвращается в структуре, на которую указывает параметр *бестрауте* .</span><span class="sxs-lookup"><span data-stu-id="488ef-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="488ef-126"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="488ef-127">Маршрут к указанной сети отсутствует, или операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="488ef-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="488ef-128">Чтобы получить дополнительные сведения, вызовите [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="488ef-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="488ef-129"><dt>**БЕЗ \_ ошибок**</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="488ef-130">Операция завершилась удачно, но маршрут к указанной сети отсутствует.</span><span class="sxs-lookup"><span data-stu-id="488ef-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="488ef-131"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="488ef-132">Значение параметра *протоколфамили* не соответствует ни одному установленному семейству протоколов.</span><span class="sxs-lookup"><span data-stu-id="488ef-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="488ef-133"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="488ef-134">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="488ef-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="488ef-135">Требования</span><span class="sxs-lookup"><span data-stu-id="488ef-135">Requirements</span></span>



| <span data-ttu-id="488ef-136">Требование</span><span class="sxs-lookup"><span data-stu-id="488ef-136">Requirement</span></span> | <span data-ttu-id="488ef-137">Значение</span><span class="sxs-lookup"><span data-stu-id="488ef-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="488ef-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="488ef-138">Minimum supported client</span></span><br/> | <span data-ttu-id="488ef-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="488ef-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="488ef-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="488ef-140">Minimum supported server</span></span><br/> | <span data-ttu-id="488ef-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="488ef-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="488ef-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="488ef-142">End of server support</span></span><br/>    | <span data-ttu-id="488ef-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="488ef-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="488ef-144">Header</span><span class="sxs-lookup"><span data-stu-id="488ef-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="488ef-145"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="488ef-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="488ef-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="488ef-147"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="488ef-148">DLL</span><span class="sxs-lookup"><span data-stu-id="488ef-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="488ef-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="488ef-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488ef-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="488ef-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488ef-151">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="488ef-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="488ef-152">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="488ef-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="488ef-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="488ef-153">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="488ef-154">**IP- \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="488ef-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="488ef-155">**\_сеть IPX**</span><span class="sxs-lookup"><span data-stu-id="488ef-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="488ef-156">Идентификаторы семейства протоколов RTMv1</span><span class="sxs-lookup"><span data-stu-id="488ef-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

