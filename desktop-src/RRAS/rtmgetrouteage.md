---
title: Функция Ртмжетраутеаже (RTM. h)
description: Функция Ртмжетраутеаже Возвращает возраст маршрута. Возраст — это время в секундах с момента создания или последнего обновления.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RAS функции Ртмжетраутеаже
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802788"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="a94e0-105">Функция Ртмжетраутеаже</span><span class="sxs-lookup"><span data-stu-id="a94e0-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="a94e0-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a94e0-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a94e0-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="a94e0-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a94e0-108">Функция **ртмжетраутеаже** Возвращает возраст маршрута.</span><span class="sxs-lookup"><span data-stu-id="a94e0-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="a94e0-109">Возраст — это время в секундах с момента создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="a94e0-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94e0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a94e0-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="a94e0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a94e0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94e0-112">*Маршрут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a94e0-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a94e0-113">Указатель на структуру, относящуюся к конкретному семейству протоколов, которая указывает данные маршрута, недавно полученные из диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="a94e0-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94e0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a94e0-114">Return value</span></span>

<span data-ttu-id="a94e0-115">Возвращаемое значение является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a94e0-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="a94e0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a94e0-116">Value</span></span>                                                                                   | <span data-ttu-id="a94e0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a94e0-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a94e0-118"><dt>**Маршрутизация**</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="a94e0-119">Время в секундах с момента создания или последнего обновления маршрута.</span><span class="sxs-lookup"><span data-stu-id="a94e0-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="a94e0-120"><dt>**INFINITE**</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="a94e0-121">Недопустимое содержимое структуры маршрута.</span><span class="sxs-lookup"><span data-stu-id="a94e0-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="a94e0-122">В этом случае вызов [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку " \_ Недопустимый \_ параметр".</span><span class="sxs-lookup"><span data-stu-id="a94e0-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a94e0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a94e0-123">Remarks</span></span>

<span data-ttu-id="a94e0-124">Срок действия маршрута вычисляются на основе \_ элемента метки времени RR структуры, на которую указывает параметр *Route* .</span><span class="sxs-lookup"><span data-stu-id="a94e0-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="a94e0-125">Диспетчер таблиц маршрутизации задает значение этого элемента при добавлении или обновлении маршрута.</span><span class="sxs-lookup"><span data-stu-id="a94e0-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="a94e0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a94e0-126">Requirements</span></span>



| <span data-ttu-id="a94e0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a94e0-127">Requirement</span></span> | <span data-ttu-id="a94e0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a94e0-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a94e0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a94e0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a94e0-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a94e0-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a94e0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a94e0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a94e0-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a94e0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a94e0-133">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a94e0-133">End of server support</span></span><br/>    | <span data-ttu-id="a94e0-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a94e0-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="a94e0-135">Header</span><span class="sxs-lookup"><span data-stu-id="a94e0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a94e0-136"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="a94e0-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a94e0-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a94e0-138"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="a94e0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a94e0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a94e0-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a94e0-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a94e0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94e0-142">Справочник по диспетчеру таблиц маршрутизации версии \_ 1</span><span class="sxs-lookup"><span data-stu-id="a94e0-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a94e0-143">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="a94e0-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="a94e0-144">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a94e0-144">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="a94e0-145">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="a94e0-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="a94e0-146">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="a94e0-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

