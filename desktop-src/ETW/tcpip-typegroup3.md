---
description: Этот класс является классом типа событий для событий TCP/IP IPv6. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: Класс TcpIp_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984784"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="179e8-104">\_Класс TcpIp TypeGroup3</span><span class="sxs-lookup"><span data-stu-id="179e8-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="179e8-105">Этот класс является классом типа событий для событий TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="179e8-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="179e8-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="179e8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="179e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="179e8-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="179e8-108">Участники</span><span class="sxs-lookup"><span data-stu-id="179e8-108">Members</span></span>

<span data-ttu-id="179e8-109">Класс **TcpIp \_ TypeGroup3** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="179e8-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="179e8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="179e8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="179e8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="179e8-111">Properties</span></span>

<span data-ttu-id="179e8-112">Класс **TcpIp \_ TypeGroup3** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="179e8-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="179e8-113">коннид</span><span class="sxs-lookup"><span data-stu-id="179e8-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="179e8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-116">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="179e8-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="179e8-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="179e8-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-118">даддр</span><span class="sxs-lookup"><span data-stu-id="179e8-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="179e8-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="179e8-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="179e8-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="179e8-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="179e8-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="179e8-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="179e8-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="179e8-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="179e8-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-128">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="179e8-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="179e8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="179e8-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="179e8-132">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="179e8-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-133">саддр</span><span class="sxs-lookup"><span data-stu-id="179e8-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="179e8-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-136">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="179e8-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="179e8-137">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="179e8-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-138">секнум</span><span class="sxs-lookup"><span data-stu-id="179e8-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="179e8-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-141">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="179e8-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="179e8-142">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="179e8-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-143">size</span><span class="sxs-lookup"><span data-stu-id="179e8-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="179e8-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-146">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="179e8-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="179e8-147">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="179e8-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="179e8-148">назван</span><span class="sxs-lookup"><span data-stu-id="179e8-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="179e8-149">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="179e8-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="179e8-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="179e8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="179e8-151">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="179e8-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="179e8-152">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="179e8-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="179e8-153">Требования</span><span class="sxs-lookup"><span data-stu-id="179e8-153">Requirements</span></span>



| <span data-ttu-id="179e8-154">Требование</span><span class="sxs-lookup"><span data-stu-id="179e8-154">Requirement</span></span> | <span data-ttu-id="179e8-155">Значение</span><span class="sxs-lookup"><span data-stu-id="179e8-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="179e8-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="179e8-156">Minimum supported client</span></span><br/> | <span data-ttu-id="179e8-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="179e8-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="179e8-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="179e8-158">Minimum supported server</span></span><br/> | <span data-ttu-id="179e8-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="179e8-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="179e8-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="179e8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="179e8-161">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="179e8-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




