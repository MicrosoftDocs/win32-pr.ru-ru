---
description: Является устаревшим и не должен использоваться.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Структура адреса (Netmon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663456"
---
# <a name="address-structure"></a><span data-ttu-id="d21de-103">Структура адреса</span><span class="sxs-lookup"><span data-stu-id="d21de-103">ADDRESS structure</span></span>

<span data-ttu-id="d21de-104">Структура **адресов** устарела и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="d21de-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d21de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d21de-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="d21de-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d21de-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d21de-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d21de-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-108">Тип адреса.</span><span class="sxs-lookup"><span data-stu-id="d21de-108">Address type.</span></span> <span data-ttu-id="d21de-109">Значением может быть одно из следующих.</span><span class="sxs-lookup"><span data-stu-id="d21de-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="d21de-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="d21de-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="d21de-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="d21de-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="d21de-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="d21de-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="d21de-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="d21de-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="d21de-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="d21de-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="d21de-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="d21de-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="d21de-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="d21de-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="d21de-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="d21de-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="d21de-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="d21de-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="d21de-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="d21de-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="d21de-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d21de-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="d21de-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="d21de-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="d21de-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="d21de-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="d21de-123">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="d21de-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-124">Представление данных, выраженное в виде необработанного MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="d21de-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-125">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="d21de-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-126">Представление данных, выраженное в виде необработанного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d21de-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-127">**ипксраваддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-128">Представление данных, выраженное в виде необработанного IPX-адреса.</span><span class="sxs-lookup"><span data-stu-id="d21de-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-129">**ипксаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-130">Представление данных, выраженное в виде декодированного значения IPX-адреса.</span><span class="sxs-lookup"><span data-stu-id="d21de-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-131">**винесиправаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-132">Представление данных, выраженное в виде IP-адреса необработанных Vines.</span><span class="sxs-lookup"><span data-stu-id="d21de-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-133">**винесипаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-134">Представление данных, выраженное в виде IP-адреса декодированных Vines.</span><span class="sxs-lookup"><span data-stu-id="d21de-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-135">**есернетсркаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-136">Представление данных, выраженное в виде адреса источника Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d21de-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-137">**есернетдстаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-138">Представление данных, выраженное в виде адреса назначения Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d21de-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-139">**токенрингсркаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-140">Представление данных в виде адреса источника Token Ring.</span><span class="sxs-lookup"><span data-stu-id="d21de-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-141">**токенрингдстаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-142">Представление данных в виде адреса назначения Token Ring.</span><span class="sxs-lookup"><span data-stu-id="d21de-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-143">**фддисркаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-144">Представление данных, выраженное в виде исходного адреса FDDI.</span><span class="sxs-lookup"><span data-stu-id="d21de-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-145">**фддидстаддресс**</span><span class="sxs-lookup"><span data-stu-id="d21de-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-146">Представление данных, выраженное в виде адреса назначения FDDI.</span><span class="sxs-lookup"><span data-stu-id="d21de-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="d21de-147">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="d21de-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d21de-148">Набор флагов, которые изменяют свойства адреса.</span><span class="sxs-lookup"><span data-stu-id="d21de-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d21de-149">Требования</span><span class="sxs-lookup"><span data-stu-id="d21de-149">Requirements</span></span>



| <span data-ttu-id="d21de-150">Требование</span><span class="sxs-lookup"><span data-stu-id="d21de-150">Requirement</span></span> | <span data-ttu-id="d21de-151">Значение</span><span class="sxs-lookup"><span data-stu-id="d21de-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d21de-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d21de-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d21de-153">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d21de-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d21de-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d21de-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d21de-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d21de-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d21de-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d21de-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d21de-157"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d21de-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




