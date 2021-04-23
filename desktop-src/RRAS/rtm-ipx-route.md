---
title: Структура RTM_IPX_ROUTE (RTM. h)
description: '\_ \_ Структура маршрута RTM IPX содержит сведения, описывающие маршрут для семейства протоколов IPX.'
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RAS структуры RTM_IPX_ROUTE
- RAS — указатель структуры PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988430"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="e5d9b-105">\_ \_ Структура маршрута RTM IPX</span><span class="sxs-lookup"><span data-stu-id="e5d9b-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="e5d9b-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e5d9b-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="e5d9b-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e5d9b-108">Структура **\_ \_ маршрута RTM IPX** содержит сведения, описывающие маршрут для семейства протоколов IPX.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d9b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5d9b-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="e5d9b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e5d9b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e5d9b-111">**\_Метка времени RR**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-112">Указывает время создания или последнего обновления записи маршрута.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="e5d9b-113">Этот элемент задается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="e5d9b-114">Время выражается в виде структуры FILETIME.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5d9b-115">**RR \_ раутингпротокол**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-116">Указывает протокол маршрутизации, который добавил маршрут.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="e5d9b-117">**RR \_ InterfaceID**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-118">Указывает интерфейс, через который был получен маршрут.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="e5d9b-119">**RR \_ протоколспеЦификдата**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-120">Указывает [**специфичную для протокола структуру \_ \_ данных**](protocol-specific-data.md) , которая содержит память, зарезервированную для данных, относящихся к протоколам маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="e5d9b-121">**RR, \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-122">Указывает структуру [**\_ сети IPX**](ipx-network.md) , которая содержит IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="e5d9b-123">**RR \_ некссопаддресс**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-124">Указывает структуру [**\_ \_ \_ адресов следующего прыжка IPX**](ipx-next-hop-address.md) , которая содержит адрес маршрутизатора следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="e5d9b-125">**RR \_ фамилиспеЦификдата**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="e5d9b-126">Указывает структуру [**\_ \_ данных, характерную**](ipx-specific-data.md) для протокола IPX, которая содержит данные, относящиеся к семейству протоколов IPX.</span><span class="sxs-lookup"><span data-stu-id="e5d9b-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5d9b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5d9b-127">Remarks</span></span>

<span data-ttu-id="e5d9b-128">Элементы структуры **маршрута RTM- \_ IPX \_** выводятся полностью по **значению DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e5d9b-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d9b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e5d9b-129">Requirements</span></span>



| <span data-ttu-id="e5d9b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e5d9b-130">Requirement</span></span> | <span data-ttu-id="e5d9b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d9b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e5d9b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5d9b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d9b-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e5d9b-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="e5d9b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5d9b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d9b-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5d9b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5d9b-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e5d9b-136">End of server support</span></span><br/>    | <span data-ttu-id="e5d9b-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5d9b-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="e5d9b-138">Header</span><span class="sxs-lookup"><span data-stu-id="e5d9b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d9b-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d9b-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d9b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5d9b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d9b-141">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="e5d9b-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e5d9b-142">Структуры диспетчера таблиц маршрутизации версии \_ 1 \_</span><span class="sxs-lookup"><span data-stu-id="e5d9b-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="e5d9b-143">**\_сеть IPX**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="e5d9b-144">**\_адрес следующего \_ ПРЫЖКа IPX \_**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="e5d9b-145">**\_данные, относящиеся к IPX \_**</span><span class="sxs-lookup"><span data-stu-id="e5d9b-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





