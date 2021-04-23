---
title: Функция Ртмжетнетворккаунт (RTM. h)
description: Функция Ртмжетнетворккаунт Извлекает число сетей, к которым диспетчер таблиц маршрутизации имеет маршруты.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RAS функции Ртмжетнетворккаунт
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802207"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="c9931-104">Функция Ртмжетнетворккаунт</span><span class="sxs-lookup"><span data-stu-id="c9931-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="c9931-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c9931-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c9931-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="c9931-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c9931-107">Функция **ртмжетнетворккаунт** Извлекает число сетей, к которым диспетчер таблиц маршрутизации имеет маршруты.</span><span class="sxs-lookup"><span data-stu-id="c9931-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9931-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9931-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="c9931-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9931-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9931-110">*Протоколфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9931-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9931-111">Указывает тип сети для получения сведений о маршруте, например IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="c9931-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9931-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9931-112">Return value</span></span>

<span data-ttu-id="c9931-113">Если функция выполнена удачно, возвращается значение счетчика сети, а также число сетей, известных протоколам маршрутизации указанного семейства протоколов.</span><span class="sxs-lookup"><span data-stu-id="c9931-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="c9931-114">Если возвращаемое значение равно нулю, маршруты недоступны или операция завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c9931-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="c9931-115">Чтобы получить дополнительные сведения, вызовите [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="c9931-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="c9931-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c9931-116">Value</span></span>                                                                                                    | <span data-ttu-id="c9931-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c9931-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9931-118"><dt>**БЕЗ \_ ошибок**</dt></span><span class="sxs-lookup"><span data-stu-id="c9931-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="c9931-119">Операция завершилась удачно, но маршруты недоступны.</span><span class="sxs-lookup"><span data-stu-id="c9931-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="c9931-120"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="c9931-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="c9931-121">Значение параметра *протоколфамили* не соответствует ни одному установленному семейству протоколов.</span><span class="sxs-lookup"><span data-stu-id="c9931-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9931-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c9931-122">Requirements</span></span>



| <span data-ttu-id="c9931-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c9931-123">Requirement</span></span> | <span data-ttu-id="c9931-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c9931-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9931-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9931-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c9931-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9931-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c9931-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9931-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c9931-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9931-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9931-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c9931-129">End of server support</span></span><br/>    | <span data-ttu-id="c9931-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9931-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c9931-131">Header</span><span class="sxs-lookup"><span data-stu-id="c9931-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9931-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9931-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9931-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9931-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9931-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9931-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9931-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c9931-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9931-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9931-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9931-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9931-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9931-138">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="c9931-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c9931-139">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="c9931-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="c9931-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c9931-140">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="c9931-141">Идентификаторы семейства протоколов RTMv1</span><span class="sxs-lookup"><span data-stu-id="c9931-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

