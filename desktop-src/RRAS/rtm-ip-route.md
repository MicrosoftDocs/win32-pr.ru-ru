---
title: Структура RTM_IP_ROUTE (RTM. h)
description: '\_Структура IP- \_ маршрута RTM содержит сведения, описывающие маршрут, принадлежащий семейству протоколов IP.'
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RAS структуры RTM_IP_ROUTE
- RAS — указатель структуры PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672909"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="8b0e7-105">\_Структура IP- \_ маршрута RTM</span><span class="sxs-lookup"><span data-stu-id="8b0e7-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="8b0e7-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="8b0e7-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="8b0e7-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="8b0e7-108">Структура **\_ IP- \_ маршрута RTM** содержит сведения, описывающие маршрут, принадлежащий семейству протоколов IP.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0e7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b0e7-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="8b0e7-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8b0e7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b0e7-111">**\_Метка времени RR**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-112">Указывает время создания или последнего обновления записи маршрута.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="8b0e7-113">Этот элемент задается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="8b0e7-114">Время выражается в виде структуры FILETIME.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e7-115">**RR \_ раутингпротокол**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-116">Указывает протокол маршрутизации, который добавил маршрут.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e7-117">**RR \_ InterfaceID**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-118">Указывает интерфейс, через который был получен маршрут.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e7-119">**RR \_ протоколспеЦификдата**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-120">Указывает структуру [**\_ \_ данных, характерную для протокола**](protocol-specific-data.md) , которая содержит память, зарезервированную для данных, зависящих от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e7-121">**RR, \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-122">Указывает структуру [**IP- \_ сети**](ip-network.md) , которая содержит адрес IP-сети.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e7-123">**RR \_ некссопаддресс**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-124">Указывает структуру [**IP \_ - \_ \_ адреса следующего прыжка**](ip-next-hop-address.md) , которая содержит адрес маршрутизатора следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="8b0e7-125">**RR \_ фамилиспеЦификдата**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="8b0e7-126">Указывает структуру [**\_ \_ данных, относящуюся к конкретному IP-адресу**](ip-specific-data.md) , которая содержит данные, относящиеся к семейству IP-протоколов.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b0e7-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b0e7-127">Remarks</span></span>

<span data-ttu-id="8b0e7-128">Члены структуры **\_ IP- \_ маршрута RTM** имеют все, что выровняйтеся по **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8b0e7-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0e7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8b0e7-129">Requirements</span></span>



| <span data-ttu-id="8b0e7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8b0e7-130">Requirement</span></span> | <span data-ttu-id="8b0e7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0e7-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8b0e7-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b0e7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0e7-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8b0e7-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="8b0e7-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b0e7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0e7-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b0e7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8b0e7-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8b0e7-136">End of server support</span></span><br/>    | <span data-ttu-id="8b0e7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b0e7-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="8b0e7-138">Header</span><span class="sxs-lookup"><span data-stu-id="8b0e7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b0e7-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b0e7-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b0e7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b0e7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0e7-141">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="8b0e7-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="8b0e7-142">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="8b0e7-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="8b0e7-143">**IP- \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="8b0e7-144">**\_адрес следующего \_ ПРЫЖКа IP \_**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="8b0e7-145">**\_данные конкретного IP-адреса \_**</span><span class="sxs-lookup"><span data-stu-id="8b0e7-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





