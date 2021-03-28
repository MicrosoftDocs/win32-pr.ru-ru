---
description: Этот класс является классом типа события для событий протокола IPv6 TCP/IP Connect и Accept. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: Класс TcpIp_TypeGroup4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811837"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="34389-104">\_Класс TcpIp TypeGroup4</span><span class="sxs-lookup"><span data-stu-id="34389-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="34389-105">Этот класс является классом типа события для событий протокола IPv6 TCP/IP Connect и Accept.</span><span class="sxs-lookup"><span data-stu-id="34389-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="34389-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="34389-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="34389-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34389-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="34389-108">Участники</span><span class="sxs-lookup"><span data-stu-id="34389-108">Members</span></span>

<span data-ttu-id="34389-109">Класс **TcpIp \_ TypeGroup4** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="34389-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="34389-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="34389-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34389-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="34389-111">Properties</span></span>

<span data-ttu-id="34389-112">Класс **TcpIp \_ TypeGroup4** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="34389-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34389-113">коннид</span><span class="sxs-lookup"><span data-stu-id="34389-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34389-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34389-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-116">Квалификаторы: Вмидатаид (15), Pointer</span><span class="sxs-lookup"><span data-stu-id="34389-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="34389-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="34389-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="34389-118">даддр</span><span class="sxs-lookup"><span data-stu-id="34389-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="34389-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="34389-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-121">Квалификаторы: Вмидатаид (3), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="34389-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="34389-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="34389-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="34389-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="34389-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="34389-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="34389-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-126">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="34389-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="34389-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="34389-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="34389-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="34389-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34389-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34389-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-131">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="34389-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="34389-132">Максимальный размер сегмента.</span><span class="sxs-lookup"><span data-stu-id="34389-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="34389-133">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="34389-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34389-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34389-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-136">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="34389-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="34389-137">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="34389-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="34389-138">**ркввин**</span><span class="sxs-lookup"><span data-stu-id="34389-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34389-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34389-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-141">Квалификаторы: Вмидатаид (11)</span><span class="sxs-lookup"><span data-stu-id="34389-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="34389-142">Размер окна приема TCP.</span><span class="sxs-lookup"><span data-stu-id="34389-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="34389-143">**ркввинскале**</span><span class="sxs-lookup"><span data-stu-id="34389-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-144">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="34389-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="34389-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-146">Квалификаторы: Вмидатаид (12)</span><span class="sxs-lookup"><span data-stu-id="34389-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="34389-147">Коэффициент масштабирования окна приема TCP.</span><span class="sxs-lookup"><span data-stu-id="34389-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="34389-148">**саккопт**</span><span class="sxs-lookup"><span data-stu-id="34389-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34389-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34389-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-151">Квалификаторы: **вмидатаид** (8)</span><span class="sxs-lookup"><span data-stu-id="34389-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="34389-152">Параметр селективного подтверждения (SACK) в заголовке TCP.</span><span class="sxs-lookup"><span data-stu-id="34389-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="34389-153">саддр</span><span class="sxs-lookup"><span data-stu-id="34389-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-154">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="34389-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="34389-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-156">Квалификаторы: Вмидатаид (4), Extension ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="34389-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="34389-157">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="34389-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="34389-158">секнум</span><span class="sxs-lookup"><span data-stu-id="34389-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34389-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34389-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-161">Квалификаторы: Вмидатаид (14)</span><span class="sxs-lookup"><span data-stu-id="34389-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="34389-162">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="34389-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="34389-163">size</span><span class="sxs-lookup"><span data-stu-id="34389-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-164">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34389-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34389-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-166">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="34389-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="34389-167">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="34389-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="34389-168">**сндвинскале**</span><span class="sxs-lookup"><span data-stu-id="34389-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-169">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="34389-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="34389-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-171">Квалификаторы: Вмидатаид (13)</span><span class="sxs-lookup"><span data-stu-id="34389-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="34389-172">Коэффициент масштабирования окна отправки TCP.</span><span class="sxs-lookup"><span data-stu-id="34389-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="34389-173">назван</span><span class="sxs-lookup"><span data-stu-id="34389-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-174">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="34389-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="34389-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-176">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="34389-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="34389-177">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="34389-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="34389-178">**тсопт**</span><span class="sxs-lookup"><span data-stu-id="34389-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34389-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34389-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-181">Квалификаторы: Вмидатаид (9)</span><span class="sxs-lookup"><span data-stu-id="34389-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="34389-182">Параметр временной метки в заголовке TCP.</span><span class="sxs-lookup"><span data-stu-id="34389-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="34389-183">**всопт**</span><span class="sxs-lookup"><span data-stu-id="34389-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34389-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34389-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34389-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34389-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34389-186">Квалификаторы: Вмидатаид (10)</span><span class="sxs-lookup"><span data-stu-id="34389-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="34389-187">Параметр масштабирования окна в заголовке TCP.</span><span class="sxs-lookup"><span data-stu-id="34389-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34389-188">Требования</span><span class="sxs-lookup"><span data-stu-id="34389-188">Requirements</span></span>



| <span data-ttu-id="34389-189">Требование</span><span class="sxs-lookup"><span data-stu-id="34389-189">Requirement</span></span> | <span data-ttu-id="34389-190">Значение</span><span class="sxs-lookup"><span data-stu-id="34389-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="34389-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34389-191">Minimum supported client</span></span><br/> | <span data-ttu-id="34389-192">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34389-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="34389-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34389-193">Minimum supported server</span></span><br/> | <span data-ttu-id="34389-194">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34389-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34389-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34389-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34389-196">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="34389-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




