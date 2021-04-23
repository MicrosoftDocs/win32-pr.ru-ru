---
description: Этот класс является классом типа событий для событий отправки TCP/IP IPv4. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: Класс TcpIp_SendIPV4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991469"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="38413-104">\_Класс TcpIp SendIPV4</span><span class="sxs-lookup"><span data-stu-id="38413-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="38413-105">Этот класс является классом типа событий для событий отправки TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="38413-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="38413-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="38413-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="38413-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38413-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="38413-108">Участники</span><span class="sxs-lookup"><span data-stu-id="38413-108">Members</span></span>

<span data-ttu-id="38413-109">Класс **TcpIp \_ SendIPV4** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38413-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="38413-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="38413-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38413-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="38413-111">Properties</span></span>

<span data-ttu-id="38413-112">Класс **TcpIp \_ SendIPV4** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38413-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38413-113">коннид</span><span class="sxs-lookup"><span data-stu-id="38413-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38413-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38413-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-116">Квалификаторы: Вмидатаид (10), Pointer</span><span class="sxs-lookup"><span data-stu-id="38413-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="38413-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="38413-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="38413-118">даддр</span><span class="sxs-lookup"><span data-stu-id="38413-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="38413-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="38413-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="38413-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="38413-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="38413-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="38413-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="38413-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="38413-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="38413-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="38413-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="38413-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="38413-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="38413-128">**завершения**</span><span class="sxs-lookup"><span data-stu-id="38413-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38413-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38413-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-131">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="38413-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="38413-132">Время запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="38413-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="38413-133">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="38413-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38413-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38413-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-136">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="38413-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="38413-137">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="38413-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="38413-138">саддр</span><span class="sxs-lookup"><span data-stu-id="38413-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-139">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="38413-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="38413-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-141">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="38413-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="38413-142">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="38413-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="38413-143">секнум</span><span class="sxs-lookup"><span data-stu-id="38413-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38413-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38413-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-146">Квалификаторы: Вмидатаид (9)</span><span class="sxs-lookup"><span data-stu-id="38413-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="38413-147">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="38413-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="38413-148">size</span><span class="sxs-lookup"><span data-stu-id="38413-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38413-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38413-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-151">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="38413-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="38413-152">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="38413-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="38413-153">назван</span><span class="sxs-lookup"><span data-stu-id="38413-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-154">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="38413-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="38413-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-156">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="38413-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="38413-157">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="38413-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="38413-158">**стартиме**</span><span class="sxs-lookup"><span data-stu-id="38413-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38413-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38413-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38413-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38413-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38413-161">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="38413-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="38413-162">Начать время запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="38413-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38413-163">Требования</span><span class="sxs-lookup"><span data-stu-id="38413-163">Requirements</span></span>



| <span data-ttu-id="38413-164">Требование</span><span class="sxs-lookup"><span data-stu-id="38413-164">Requirement</span></span> | <span data-ttu-id="38413-165">Значение</span><span class="sxs-lookup"><span data-stu-id="38413-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38413-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38413-166">Minimum supported client</span></span><br/> | <span data-ttu-id="38413-167">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38413-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38413-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38413-168">Minimum supported server</span></span><br/> | <span data-ttu-id="38413-169">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38413-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38413-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38413-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38413-171">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="38413-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




