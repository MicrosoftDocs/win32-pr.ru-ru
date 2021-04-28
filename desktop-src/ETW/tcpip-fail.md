---
description: Класс TcpIp_Fail — этот класс является классом типа событий для событий сбоя TCP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: Класс TcpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105852"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="d5055-104">\_Неудачный класс TcpIp</span><span class="sxs-lookup"><span data-stu-id="d5055-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="d5055-105">Этот класс является классом типа событий для событий сбоя TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d5055-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="d5055-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="d5055-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5055-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5055-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="d5055-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d5055-108">Members</span></span>

<span data-ttu-id="d5055-109">Класс **TcpIp \_ Fail** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5055-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="d5055-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5055-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5055-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="d5055-111">Properties</span></span>

<span data-ttu-id="d5055-112">Класс **TcpIp \_ Fail** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d5055-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5055-113">**фаилурекоде**</span><span class="sxs-lookup"><span data-stu-id="d5055-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5055-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d5055-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d5055-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5055-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5055-116">Причина сбоя.</span><span class="sxs-lookup"><span data-stu-id="d5055-116">Reason for the failure.</span></span> <span data-ttu-id="d5055-117">Может иметь один из следующих кодов:</span><span class="sxs-lookup"><span data-stu-id="d5055-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="d5055-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Ошибка при \_ НЕДОСТАТОЧНО \_ ресурсов** (1)</span><span class="sxs-lookup"><span data-stu-id="d5055-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d5055-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Ошибка при \_ СЛИШКОМ \_ много \_ адресов** (2)</span><span class="sxs-lookup"><span data-stu-id="d5055-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d5055-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Ошибка при \_ АДРЕС \_ существует** (3)</span><span class="sxs-lookup"><span data-stu-id="d5055-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d5055-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Ошибка при \_ Недопустимый \_ адрес** (4)</span><span class="sxs-lookup"><span data-stu-id="d5055-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d5055-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Ошибка при \_ ДРУГОЕ** (5)</span><span class="sxs-lookup"><span data-stu-id="d5055-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d5055-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Ошибка при \_ \_Адрес тимеваит \_ существует** (6)</span><span class="sxs-lookup"><span data-stu-id="d5055-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d5055-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="d5055-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5055-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d5055-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d5055-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5055-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5055-127">Определяет протокол.</span><span class="sxs-lookup"><span data-stu-id="d5055-127">Identifies the protocol.</span></span> <span data-ttu-id="d5055-128">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d5055-128">Can be one of the following values:</span></span>



| <span data-ttu-id="d5055-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d5055-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="d5055-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d5055-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="d5055-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d5055-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="d5055-132">Семейство адресов протокола IP версии 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="d5055-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="d5055-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="d5055-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="d5055-134">Семейство адресов IP версии 6 (IPv6)..</span><span class="sxs-lookup"><span data-stu-id="d5055-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5055-135">Требования</span><span class="sxs-lookup"><span data-stu-id="d5055-135">Requirements</span></span>



| <span data-ttu-id="d5055-136">Требование</span><span class="sxs-lookup"><span data-stu-id="d5055-136">Requirement</span></span> | <span data-ttu-id="d5055-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d5055-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5055-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5055-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d5055-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5055-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5055-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5055-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d5055-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5055-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5055-142">См. также</span><span class="sxs-lookup"><span data-stu-id="d5055-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5055-143">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="d5055-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




