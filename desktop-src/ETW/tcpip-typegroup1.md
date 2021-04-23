---
description: Этот класс является классом типа событий для событий TCP/IP IPv4. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: Класс TcpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984792"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="45d1d-104">\_Класс TcpIp TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="45d1d-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="45d1d-105">Этот класс является классом типа событий для событий TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="45d1d-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="45d1d-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="45d1d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d1d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45d1d-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
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

## <a name="members"></a><span data-ttu-id="45d1d-108">Участники</span><span class="sxs-lookup"><span data-stu-id="45d1d-108">Members</span></span>

<span data-ttu-id="45d1d-109">Класс **TcpIp \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="45d1d-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="45d1d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="45d1d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45d1d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="45d1d-111">Properties</span></span>

<span data-ttu-id="45d1d-112">Класс **TcpIp \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="45d1d-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45d1d-113">коннид</span><span class="sxs-lookup"><span data-stu-id="45d1d-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d1d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-116">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="45d1d-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="45d1d-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-118">даддр</span><span class="sxs-lookup"><span data-stu-id="45d1d-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="45d1d-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="45d1d-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="45d1d-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="45d1d-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="45d1d-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="45d1d-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="45d1d-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-128">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="45d1d-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d1d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="45d1d-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-132">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="45d1d-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-133">саддр</span><span class="sxs-lookup"><span data-stu-id="45d1d-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="45d1d-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-136">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="45d1d-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-137">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="45d1d-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-138">секнум</span><span class="sxs-lookup"><span data-stu-id="45d1d-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d1d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-141">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="45d1d-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-142">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="45d1d-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-143">size</span><span class="sxs-lookup"><span data-stu-id="45d1d-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d1d-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-146">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="45d1d-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-147">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="45d1d-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="45d1d-148">назван</span><span class="sxs-lookup"><span data-stu-id="45d1d-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d1d-149">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="45d1d-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45d1d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d1d-151">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="45d1d-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="45d1d-152">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="45d1d-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45d1d-153">Требования</span><span class="sxs-lookup"><span data-stu-id="45d1d-153">Requirements</span></span>



| <span data-ttu-id="45d1d-154">Требование</span><span class="sxs-lookup"><span data-stu-id="45d1d-154">Requirement</span></span> | <span data-ttu-id="45d1d-155">Значение</span><span class="sxs-lookup"><span data-stu-id="45d1d-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45d1d-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45d1d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="45d1d-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45d1d-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="45d1d-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45d1d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="45d1d-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45d1d-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45d1d-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45d1d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d1d-161">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="45d1d-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




