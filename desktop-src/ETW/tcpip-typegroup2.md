---
description: Этот класс является классом типа событий для событий IPv4 TCP/IP Connect и Accept. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Класс TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544319"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="2b71b-104">\_Класс TcpIp TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="2b71b-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="2b71b-105">Этот класс является классом типа событий для событий IPv4 TCP/IP Connect и Accept.</span><span class="sxs-lookup"><span data-stu-id="2b71b-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="2b71b-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="2b71b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b71b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b71b-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

## <a name="members"></a><span data-ttu-id="2b71b-108">Участники</span><span class="sxs-lookup"><span data-stu-id="2b71b-108">Members</span></span>

<span data-ttu-id="2b71b-109">Класс **TcpIp \_ TypeGroup2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b71b-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="2b71b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b71b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b71b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b71b-111">Properties</span></span>

<span data-ttu-id="2b71b-112">Класс **TcpIp \_ TypeGroup2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b71b-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b71b-113">**коннид**</span><span class="sxs-lookup"><span data-stu-id="2b71b-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b71b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-116">Квалификаторы: **вмидатаид (15)**, **pointer**</span><span class="sxs-lookup"><span data-stu-id="2b71b-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-117">Уникальный идентификатор соединения для сопоставления событий, принадлежащих одному соединению.</span><span class="sxs-lookup"><span data-stu-id="2b71b-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-118">**даддр**</span><span class="sxs-lookup"><span data-stu-id="2b71b-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="2b71b-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-121">Квалификаторы: **вмидатаид (3)**, **Extension ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="2b71b-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2b71b-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-123">**дпорт**</span><span class="sxs-lookup"><span data-stu-id="2b71b-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="2b71b-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-126">Квалификаторы: **вмидатаид (5)**, **Extension ("порт")**</span><span class="sxs-lookup"><span data-stu-id="2b71b-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="2b71b-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="2b71b-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b71b-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-131">Квалификаторы: **вмидатаид (7)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-132">Максимальный размер сегмента.</span><span class="sxs-lookup"><span data-stu-id="2b71b-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-133">**PID**</span><span class="sxs-lookup"><span data-stu-id="2b71b-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b71b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-136">Квалификаторы: **вмидатаид (1)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-137">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="2b71b-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-138">**ркввин**</span><span class="sxs-lookup"><span data-stu-id="2b71b-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b71b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-141">Квалификаторы: **вмидатаид (11)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-142">Размер окна приема TCP.</span><span class="sxs-lookup"><span data-stu-id="2b71b-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-143">**ркввинскале**</span><span class="sxs-lookup"><span data-stu-id="2b71b-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-144">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2b71b-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-146">Квалификаторы: **вмидатаид (12)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-147">Коэффициент масштабирования окна приема TCP.</span><span class="sxs-lookup"><span data-stu-id="2b71b-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-148">**саккопт**</span><span class="sxs-lookup"><span data-stu-id="2b71b-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b71b-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-151">Квалификаторы: **вмидатаид (8)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-152">Параметр селективного подтверждения (SACK) в заголовке TCP.</span><span class="sxs-lookup"><span data-stu-id="2b71b-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-153">**саддр**</span><span class="sxs-lookup"><span data-stu-id="2b71b-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-154">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="2b71b-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-156">Квалификаторы: **вмидатаид (4)**, **Extension ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="2b71b-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-157">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2b71b-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-158">**секнум**</span><span class="sxs-lookup"><span data-stu-id="2b71b-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b71b-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-161">Квалификаторы: **вмидатаид (14)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-162">Порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="2b71b-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-163">**size**</span><span class="sxs-lookup"><span data-stu-id="2b71b-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-164">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b71b-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-166">Квалификаторы: **вмидатаид (2)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-167">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="2b71b-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-168">**сндвинскале**</span><span class="sxs-lookup"><span data-stu-id="2b71b-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-169">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2b71b-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-171">Квалификаторы: **вмидатаид (13)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-172">Коэффициент масштабирования окна отправки TCP.</span><span class="sxs-lookup"><span data-stu-id="2b71b-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-173">**назван**</span><span class="sxs-lookup"><span data-stu-id="2b71b-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-174">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="2b71b-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-176">Квалификаторы: **вмидатаид (6)**, **Extension ("порт")**</span><span class="sxs-lookup"><span data-stu-id="2b71b-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-177">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="2b71b-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-178">**тсопт**</span><span class="sxs-lookup"><span data-stu-id="2b71b-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b71b-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-181">Квалификаторы: **вмидатаид (9)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-182">Параметр временной метки в заголовке TCP.</span><span class="sxs-lookup"><span data-stu-id="2b71b-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="2b71b-183">**всопт**</span><span class="sxs-lookup"><span data-stu-id="2b71b-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b71b-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b71b-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b71b-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b71b-186">Квалификаторы: **вмидатаид (10)**</span><span class="sxs-lookup"><span data-stu-id="2b71b-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="2b71b-187">Параметр масштабирования окна в заголовке TCP.</span><span class="sxs-lookup"><span data-stu-id="2b71b-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b71b-188">Требования</span><span class="sxs-lookup"><span data-stu-id="2b71b-188">Requirements</span></span>



| <span data-ttu-id="2b71b-189">Требование</span><span class="sxs-lookup"><span data-stu-id="2b71b-189">Requirement</span></span> | <span data-ttu-id="2b71b-190">Значение</span><span class="sxs-lookup"><span data-stu-id="2b71b-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b71b-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b71b-191">Minimum supported client</span></span><br/> | <span data-ttu-id="2b71b-192">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b71b-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b71b-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b71b-193">Minimum supported server</span></span><br/> | <span data-ttu-id="2b71b-194">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b71b-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b71b-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b71b-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b71b-196">**TcpIp**</span><span class="sxs-lookup"><span data-stu-id="2b71b-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




