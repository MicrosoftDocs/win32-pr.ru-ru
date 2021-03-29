---
description: Этот класс является классом типа событий для событий Send и Receive UDP/IP IPv4. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: Класс UdpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985096"
---
# <a name="udpip_typegroup1-class"></a><span data-ttu-id="f7757-104">\_Класс удпип TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="f7757-104">UdpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="f7757-105">Этот класс является классом типа событий для событий Send и Receive UDP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="f7757-105">This class is the event type class for UDP/IP IPv4 send and receive events.</span></span>

<span data-ttu-id="f7757-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="f7757-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7757-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7757-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
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

## <a name="members"></a><span data-ttu-id="f7757-108">Участники</span><span class="sxs-lookup"><span data-stu-id="f7757-108">Members</span></span>

<span data-ttu-id="f7757-109">Класс **удпип \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f7757-109">The **UdpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f7757-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7757-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7757-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7757-111">Properties</span></span>

<span data-ttu-id="f7757-112">Класс **удпип \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f7757-112">The **UdpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7757-113">коннид</span><span class="sxs-lookup"><span data-stu-id="f7757-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7757-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-116">Квалификаторы: Вмидатаид (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="f7757-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f7757-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="f7757-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-118">даддр</span><span class="sxs-lookup"><span data-stu-id="f7757-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="f7757-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="f7757-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="f7757-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f7757-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="f7757-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="f7757-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="f7757-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f7757-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="f7757-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-128">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="f7757-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7757-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="f7757-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f7757-132">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="f7757-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-133">саддр</span><span class="sxs-lookup"><span data-stu-id="f7757-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="f7757-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-136">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="f7757-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="f7757-137">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f7757-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-138">секнум</span><span class="sxs-lookup"><span data-stu-id="f7757-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7757-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-141">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="f7757-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="f7757-142">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="f7757-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-143">size</span><span class="sxs-lookup"><span data-stu-id="f7757-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7757-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-146">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="f7757-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f7757-147">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="f7757-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-148">назван</span><span class="sxs-lookup"><span data-stu-id="f7757-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7757-149">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="f7757-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f7757-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7757-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7757-151">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="f7757-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f7757-152">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="f7757-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7757-153">Требования</span><span class="sxs-lookup"><span data-stu-id="f7757-153">Requirements</span></span>



| <span data-ttu-id="f7757-154">Требование</span><span class="sxs-lookup"><span data-stu-id="f7757-154">Requirement</span></span> | <span data-ttu-id="f7757-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f7757-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f7757-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7757-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f7757-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7757-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f7757-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7757-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f7757-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7757-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7757-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7757-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7757-161">**удпип**</span><span class="sxs-lookup"><span data-stu-id="f7757-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




