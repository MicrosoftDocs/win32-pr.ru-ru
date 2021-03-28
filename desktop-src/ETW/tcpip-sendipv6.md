---
description: Этот класс является классом типа событий для событий отправки TCP/IP IPv6. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: Класс TcpIp_SendIPV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984789"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="d1949-104">\_Класс TcpIp SendIPV6</span><span class="sxs-lookup"><span data-stu-id="d1949-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="d1949-105">Этот класс является классом типа событий для событий отправки TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="d1949-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="d1949-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="d1949-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1949-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1949-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
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

## <a name="members"></a><span data-ttu-id="d1949-108">Участники</span><span class="sxs-lookup"><span data-stu-id="d1949-108">Members</span></span>

<span data-ttu-id="d1949-109">Класс **TcpIp \_ SendIPV6** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1949-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="d1949-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1949-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1949-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1949-111">Properties</span></span>

<span data-ttu-id="d1949-112">Класс **TcpIp \_ SendIPV6** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1949-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1949-113">коннид</span><span class="sxs-lookup"><span data-stu-id="d1949-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1949-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-116">Квалификаторы: Вмидатаид (10), Pointer</span><span class="sxs-lookup"><span data-stu-id="d1949-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d1949-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="d1949-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-118">даддр</span><span class="sxs-lookup"><span data-stu-id="d1949-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="d1949-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="d1949-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="d1949-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="d1949-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="d1949-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="d1949-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="d1949-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="d1949-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="d1949-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-128">**завершения**</span><span class="sxs-lookup"><span data-stu-id="d1949-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1949-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-131">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="d1949-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="d1949-132">Время запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="d1949-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-133">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="d1949-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1949-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-136">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="d1949-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="d1949-137">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="d1949-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-138">саддр</span><span class="sxs-lookup"><span data-stu-id="d1949-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-139">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="d1949-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-141">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="d1949-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="d1949-142">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="d1949-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-143">секнум</span><span class="sxs-lookup"><span data-stu-id="d1949-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1949-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-146">Квалификаторы: Вмидатаид (9)</span><span class="sxs-lookup"><span data-stu-id="d1949-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="d1949-147">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="d1949-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-148">size</span><span class="sxs-lookup"><span data-stu-id="d1949-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1949-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-151">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="d1949-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="d1949-152">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="d1949-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-153">назван</span><span class="sxs-lookup"><span data-stu-id="d1949-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-154">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="d1949-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-156">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="d1949-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="d1949-157">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="d1949-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="d1949-158">**стартиме**</span><span class="sxs-lookup"><span data-stu-id="d1949-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1949-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1949-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1949-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1949-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1949-161">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="d1949-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="d1949-162">Начать время запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="d1949-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1949-163">Требования</span><span class="sxs-lookup"><span data-stu-id="d1949-163">Requirements</span></span>



| <span data-ttu-id="d1949-164">Требование</span><span class="sxs-lookup"><span data-stu-id="d1949-164">Requirement</span></span> | <span data-ttu-id="d1949-165">Значение</span><span class="sxs-lookup"><span data-stu-id="d1949-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d1949-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1949-166">Minimum supported client</span></span><br/> | <span data-ttu-id="d1949-167">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1949-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d1949-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1949-168">Minimum supported server</span></span><br/> | <span data-ttu-id="d1949-169">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1949-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1949-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1949-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1949-171">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="d1949-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




