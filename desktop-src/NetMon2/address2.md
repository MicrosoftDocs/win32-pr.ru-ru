---
description: Содержит один адрес любого типа поддерживаемых адресов.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: Структура ADDRESS2 (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663033"
---
# <a name="address2-structure"></a><span data-ttu-id="41cf4-103">Структура ADDRESS2</span><span class="sxs-lookup"><span data-stu-id="41cf4-103">ADDRESS2 structure</span></span>

<span data-ttu-id="41cf4-104">Структура **адреса** содержит один адрес любого типа поддерживаемых адресов.</span><span class="sxs-lookup"><span data-stu-id="41cf4-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="41cf4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41cf4-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="41cf4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="41cf4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41cf4-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="41cf4-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-108">Тип адреса.</span><span class="sxs-lookup"><span data-stu-id="41cf4-108">Address type.</span></span> <span data-ttu-id="41cf4-109">Значением может быть одно из следующих.</span><span class="sxs-lookup"><span data-stu-id="41cf4-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="41cf4-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="41cf4-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="41cf4-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="41cf4-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="41cf4-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="41cf4-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="41cf4-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="41cf4-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="41cf4-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="41cf4-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="41cf4-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="41cf4-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="41cf4-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="41cf4-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="41cf4-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="41cf4-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="41cf4-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="41cf4-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="41cf4-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="41cf4-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="41cf4-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="41cf4-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="41cf4-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="41cf4-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="41cf4-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="41cf4-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="41cf4-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="41cf4-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="41cf4-124">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="41cf4-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-125">Представление данных, выраженное в виде необработанного MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="41cf4-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-126">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="41cf4-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-127">Представление данных, выраженное в виде необработанного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="41cf4-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="41cf4-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-129">Представление данных, выраженное в виде необработанного адреса IP версии 6.</span><span class="sxs-lookup"><span data-stu-id="41cf4-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-130">**ипксраваддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-131">Представление данных, выраженное в виде необработанного IPX-адреса.</span><span class="sxs-lookup"><span data-stu-id="41cf4-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-132">**ипксаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-133">Представление данных, выраженное в виде декодированного значения IPX-адреса.</span><span class="sxs-lookup"><span data-stu-id="41cf4-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-134">**винесиправаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-135">Представление данных, выраженное в виде IP-адреса необработанных Vines.</span><span class="sxs-lookup"><span data-stu-id="41cf4-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-136">**винесипаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-137">Представление данных, выраженное в виде IP-адреса декодированных Vines.</span><span class="sxs-lookup"><span data-stu-id="41cf4-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-138">**есернетсркаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-139">Представление данных, выраженное в виде адреса источника Ethernet.</span><span class="sxs-lookup"><span data-stu-id="41cf4-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-140">**есернетдстаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-141">Представление данных, выраженное в виде адреса назначения Ethernet.</span><span class="sxs-lookup"><span data-stu-id="41cf4-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-142">**токенрингсркаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-143">Представление данных в виде адреса источника Token Ring.</span><span class="sxs-lookup"><span data-stu-id="41cf4-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-144">**токенрингдстаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-145">Представление данных в виде адреса назначения Token Ring.</span><span class="sxs-lookup"><span data-stu-id="41cf4-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-146">**фддисркаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-147">Представление данных, выраженное в виде исходного адреса FDDI.</span><span class="sxs-lookup"><span data-stu-id="41cf4-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-148">**фддидстаддресс**</span><span class="sxs-lookup"><span data-stu-id="41cf4-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="41cf4-149">Представление данных, выраженное в виде адреса назначения FDDI.</span><span class="sxs-lookup"><span data-stu-id="41cf4-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="41cf4-150">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="41cf4-150">**Flags**</span></span>
<span data-ttu-id="41cf4-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="41cf4-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="41cf4-152">Требования</span><span class="sxs-lookup"><span data-stu-id="41cf4-152">Requirements</span></span>



| <span data-ttu-id="41cf4-153">Требование</span><span class="sxs-lookup"><span data-stu-id="41cf4-153">Requirement</span></span> | <span data-ttu-id="41cf4-154">Значение</span><span class="sxs-lookup"><span data-stu-id="41cf4-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41cf4-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41cf4-155">Minimum supported client</span></span><br/> | <span data-ttu-id="41cf4-156">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41cf4-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41cf4-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41cf4-157">Minimum supported server</span></span><br/> | <span data-ttu-id="41cf4-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41cf4-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41cf4-159">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41cf4-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="41cf4-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41cf4-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




