---
description: Этот класс является классом типа событий для событий конфигурации сетевых интерфейсных карт. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Класс SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991148"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="a0bba-104">\_Класс сетевого адаптера системконфиг</span><span class="sxs-lookup"><span data-stu-id="a0bba-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="a0bba-105">Этот класс является классом типа событий для событий конфигурации сетевых интерфейсных карт.</span><span class="sxs-lookup"><span data-stu-id="a0bba-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="a0bba-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a0bba-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0bba-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="a0bba-108">Участники</span><span class="sxs-lookup"><span data-stu-id="a0bba-108">Members</span></span>

<span data-ttu-id="a0bba-109">Класс **\_ сетевого адаптера системконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a0bba-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="a0bba-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0bba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0bba-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0bba-111">Properties</span></span>

<span data-ttu-id="a0bba-112">Класс **\_ сетевого адаптера системконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a0bba-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0bba-113">днссервераддрессес</span><span class="sxs-lookup"><span data-stu-id="a0bba-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0bba-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-116">Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="a0bba-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-117">IP-адреса, используемые для запросов DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="a0bba-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="a0bba-118">Список адресов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="a0bba-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="a0bba-119">IpAddresses</span><span class="sxs-lookup"><span data-stu-id="a0bba-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0bba-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-122">Квалификаторы: Вмидатаид (6), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="a0bba-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-123">IP-адреса, связанные с сетевой картой.</span><span class="sxs-lookup"><span data-stu-id="a0bba-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="a0bba-124">Список адресов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="a0bba-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="a0bba-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="a0bba-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0bba-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-128">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="a0bba-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-129">Индекс адаптера для сетевого адаптера IPv4.</span><span class="sxs-lookup"><span data-stu-id="a0bba-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="a0bba-130">Индекс адаптера может измениться, если адаптер отключен, а затем включен или в других обстоятельствах и не должен считаться постоянным.</span><span class="sxs-lookup"><span data-stu-id="a0bba-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="a0bba-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="a0bba-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0bba-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-134">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="a0bba-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-135">Индекс адаптера для сетевого адаптера IPv6.</span><span class="sxs-lookup"><span data-stu-id="a0bba-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="a0bba-136">Индекс адаптера может измениться, если адаптер отключен, а затем включен или в других обстоятельствах и не должен считаться постоянным.</span><span class="sxs-lookup"><span data-stu-id="a0bba-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="a0bba-137">никдескриптион</span><span class="sxs-lookup"><span data-stu-id="a0bba-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0bba-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-140">Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="a0bba-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-141">Описание адаптера.</span><span class="sxs-lookup"><span data-stu-id="a0bba-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a0bba-142">фисикаладдр</span><span class="sxs-lookup"><span data-stu-id="a0bba-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0bba-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-145">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="a0bba-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-146">Аппаратный адрес для адаптера.</span><span class="sxs-lookup"><span data-stu-id="a0bba-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a0bba-147">фисикаладдрлен</span><span class="sxs-lookup"><span data-stu-id="a0bba-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0bba-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0bba-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0bba-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0bba-150">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="a0bba-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a0bba-151">Длина аппаратного адреса адаптера.</span><span class="sxs-lookup"><span data-stu-id="a0bba-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0bba-152">Требования</span><span class="sxs-lookup"><span data-stu-id="a0bba-152">Requirements</span></span>



| <span data-ttu-id="a0bba-153">Требование</span><span class="sxs-lookup"><span data-stu-id="a0bba-153">Requirement</span></span> | <span data-ttu-id="a0bba-154">Значение</span><span class="sxs-lookup"><span data-stu-id="a0bba-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a0bba-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0bba-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bba-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0bba-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a0bba-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0bba-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bba-158">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0bba-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0bba-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0bba-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bba-160">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="a0bba-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




