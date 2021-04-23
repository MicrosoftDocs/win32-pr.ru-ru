---
title: Функция Ртменумератежетнекстрауте (RTM. h)
description: Функция Ртменумератежетнекстрауте возвращает запись следующего маршрута в перечислении, запущенную вызовом Ртмкреатинумератионхандле.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RAS функции Ртменумератежетнекстрауте
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672739"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="1f8da-104">Функция Ртменумератежетнекстрауте</span><span class="sxs-lookup"><span data-stu-id="1f8da-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="1f8da-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f8da-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1f8da-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="1f8da-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1f8da-107">Функция **ртменумератежетнекстрауте** возвращает запись следующего маршрута в перечислении, запущенную вызовом [**ртмкреатинумератионхандле**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="1f8da-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f8da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f8da-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="1f8da-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f8da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f8da-110">*Енумератионхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f8da-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8da-111">Обработчик, идентифицирующий перечисление и определяющий его область действия.</span><span class="sxs-lookup"><span data-stu-id="1f8da-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="1f8da-112">Получите этот обработчик путем вызова [**ртмкреатинумератионхандле**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="1f8da-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f8da-113">*Маршрут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1f8da-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8da-114">Указатель на структуру маршрута для конкретного семейства протоколов ( [**RTM \_ - \_ маршрут IP**](rtm-ip-route.md) или [**\_ \_ маршрут RTM IPX**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="1f8da-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="1f8da-115">Эта структура получит следующий маршрут в перечислении.</span><span class="sxs-lookup"><span data-stu-id="1f8da-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f8da-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f8da-116">Return value</span></span>

<span data-ttu-id="1f8da-117">Если функция выполнена удачно, возвращается значение NO \_ Error.</span><span class="sxs-lookup"><span data-stu-id="1f8da-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="1f8da-118">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="1f8da-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="1f8da-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1f8da-119">Value</span></span>                                                                                                       | <span data-ttu-id="1f8da-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1f8da-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f8da-121"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="1f8da-122">Недопустимый параметр *енумератионхандле* .</span><span class="sxs-lookup"><span data-stu-id="1f8da-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="1f8da-123"><dt>**ОШИБКИ \_ больше \_ нет \_ маршрутов**</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="1f8da-124">В перечислении больше нет маршрутов.</span><span class="sxs-lookup"><span data-stu-id="1f8da-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="1f8da-125"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="1f8da-126">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1f8da-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f8da-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f8da-127">Remarks</span></span>

<span data-ttu-id="1f8da-128">Хотя маршруты не возвращаются в каком-либо определенном порядке, каждый маршрут в перечислении возвращается только один раз.</span><span class="sxs-lookup"><span data-stu-id="1f8da-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f8da-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1f8da-129">Requirements</span></span>



| <span data-ttu-id="1f8da-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1f8da-130">Requirement</span></span> | <span data-ttu-id="1f8da-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1f8da-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8da-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f8da-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1f8da-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1f8da-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1f8da-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f8da-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1f8da-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f8da-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f8da-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1f8da-136">End of server support</span></span><br/>    | <span data-ttu-id="1f8da-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f8da-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="1f8da-138">Header</span><span class="sxs-lookup"><span data-stu-id="1f8da-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f8da-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f8da-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f8da-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f8da-141"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f8da-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1f8da-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f8da-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f8da-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f8da-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f8da-145">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="1f8da-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1f8da-146">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="1f8da-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="1f8da-147">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="1f8da-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="1f8da-148">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="1f8da-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="1f8da-149">**ртмклосинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="1f8da-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="1f8da-150">**ртмкреатинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="1f8da-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





