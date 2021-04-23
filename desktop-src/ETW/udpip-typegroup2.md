---
description: Этот класс является классом типа событий для событий отправки и получения IPv6-адресов. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: Класс UdpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985093"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="cf309-104">\_Класс удпип TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="cf309-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="cf309-105">Этот класс является классом типа событий для событий отправки и получения IPv6-адресов.</span><span class="sxs-lookup"><span data-stu-id="cf309-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="cf309-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="cf309-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf309-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf309-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="cf309-108">Участники</span><span class="sxs-lookup"><span data-stu-id="cf309-108">Members</span></span>

<span data-ttu-id="cf309-109">Класс **удпип \_ TypeGroup2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cf309-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="cf309-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf309-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf309-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf309-111">Properties</span></span>

<span data-ttu-id="cf309-112">Класс **удпип \_ TypeGroup2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf309-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf309-113">коннид</span><span class="sxs-lookup"><span data-stu-id="cf309-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf309-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-116">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="cf309-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cf309-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="cf309-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-118">даддр</span><span class="sxs-lookup"><span data-stu-id="cf309-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cf309-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="cf309-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="cf309-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cf309-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="cf309-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cf309-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="cf309-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cf309-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="cf309-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-128">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="cf309-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf309-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="cf309-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="cf309-132">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="cf309-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-133">саддр</span><span class="sxs-lookup"><span data-stu-id="cf309-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cf309-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-136">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="cf309-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="cf309-137">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cf309-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-138">секнум</span><span class="sxs-lookup"><span data-stu-id="cf309-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf309-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-141">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="cf309-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="cf309-142">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="cf309-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-143">size</span><span class="sxs-lookup"><span data-stu-id="cf309-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf309-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-146">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="cf309-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cf309-147">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="cf309-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="cf309-148">назван</span><span class="sxs-lookup"><span data-stu-id="cf309-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf309-149">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cf309-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf309-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf309-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf309-151">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="cf309-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cf309-152">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="cf309-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf309-153">Требования</span><span class="sxs-lookup"><span data-stu-id="cf309-153">Requirements</span></span>



| <span data-ttu-id="cf309-154">Требование</span><span class="sxs-lookup"><span data-stu-id="cf309-154">Requirement</span></span> | <span data-ttu-id="cf309-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cf309-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf309-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf309-156">Minimum supported client</span></span><br/> | <span data-ttu-id="cf309-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf309-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf309-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf309-158">Minimum supported server</span></span><br/> | <span data-ttu-id="cf309-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf309-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf309-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf309-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf309-161">**удпип**</span><span class="sxs-lookup"><span data-stu-id="cf309-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




