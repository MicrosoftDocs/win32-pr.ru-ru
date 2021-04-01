---
title: Функция Ртмклосинумератионхандле (RTM. h)
description: Ртмклосинумератионхандле завершает указанное перечисление и освобождает связанные ресурсы.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RAS функции Ртмклосинумератионхандле
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071769"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="aed3e-104">Функция Ртмклосинумератионхандле</span><span class="sxs-lookup"><span data-stu-id="aed3e-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="aed3e-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aed3e-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="aed3e-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="aed3e-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="aed3e-107">**Ртмклосинумератионхандле** завершает указанное перечисление и освобождает связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aed3e-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed3e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aed3e-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="aed3e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aed3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed3e-110">*Енумератионхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aed3e-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed3e-111">Перечисление для завершения.</span><span class="sxs-lookup"><span data-stu-id="aed3e-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="aed3e-112">Получите этот обработчик путем вызова [**ртмкреатинумератионхандле**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="aed3e-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed3e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aed3e-113">Return value</span></span>

<span data-ttu-id="aed3e-114">Если функция выполнена удачно, возвращается значение NO \_ Error.</span><span class="sxs-lookup"><span data-stu-id="aed3e-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="aed3e-115">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="aed3e-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="aed3e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aed3e-116">Value</span></span>                                                                                                       | <span data-ttu-id="aed3e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="aed3e-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aed3e-118"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="aed3e-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="aed3e-119">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="aed3e-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="aed3e-120"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="aed3e-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="aed3e-121">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="aed3e-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aed3e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="aed3e-122">Requirements</span></span>



| <span data-ttu-id="aed3e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="aed3e-123">Requirement</span></span> | <span data-ttu-id="aed3e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="aed3e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aed3e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aed3e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aed3e-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aed3e-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="aed3e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aed3e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aed3e-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aed3e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aed3e-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="aed3e-129">End of server support</span></span><br/>    | <span data-ttu-id="aed3e-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aed3e-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="aed3e-131">Header</span><span class="sxs-lookup"><span data-stu-id="aed3e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed3e-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed3e-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="aed3e-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aed3e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="aed3e-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aed3e-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="aed3e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="aed3e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aed3e-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aed3e-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed3e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aed3e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed3e-138">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="aed3e-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="aed3e-139">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="aed3e-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="aed3e-140">**ртмкреатинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="aed3e-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="aed3e-141">**ртменумератежетнекстрауте**</span><span class="sxs-lookup"><span data-stu-id="aed3e-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





