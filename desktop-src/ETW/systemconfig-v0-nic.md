---
description: Этот класс является классом типа событий для событий конфигурации сетевых интерфейсных карт.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: Класс SystemConfig_V0_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985936"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="21d09-103">\_ \_ Класс сетевого адаптера системконфиг v0</span><span class="sxs-lookup"><span data-stu-id="21d09-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="21d09-104">Этот класс является классом типа событий для событий конфигурации сетевых интерфейсных карт.</span><span class="sxs-lookup"><span data-stu-id="21d09-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="21d09-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="21d09-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d09-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21d09-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="21d09-107">Участники</span><span class="sxs-lookup"><span data-stu-id="21d09-107">Members</span></span>

<span data-ttu-id="21d09-108">Класс **\_ \_ сетевого адаптера системконфиг v0** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="21d09-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="21d09-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="21d09-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21d09-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="21d09-110">Properties</span></span>

<span data-ttu-id="21d09-111">Класс **\_ \_ сетевого адаптера системконфиг v0** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="21d09-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21d09-112">**Data**</span><span class="sxs-lookup"><span data-stu-id="21d09-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21d09-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-115">Квалификаторы: **вмидатаид** (16)</span><span class="sxs-lookup"><span data-stu-id="21d09-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-116">Поле данных.</span><span class="sxs-lookup"><span data-stu-id="21d09-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="21d09-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-120">Квалификаторы: **вмидатаид** (8)</span><span class="sxs-lookup"><span data-stu-id="21d09-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-121">IP-адрес DHCP-сервера.</span><span class="sxs-lookup"><span data-stu-id="21d09-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="21d09-122">Значение 255.255.255.255 указывает, что DHCP-сервер недоступен или находится в процессе его достижения.</span><span class="sxs-lookup"><span data-stu-id="21d09-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="21d09-123">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-124">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="21d09-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-128">Квалификаторы: **вмидатаид** (12)</span><span class="sxs-lookup"><span data-stu-id="21d09-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-129">Первый IP-адрес сервера, используемый для запросов DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="21d09-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="21d09-130">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-131">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="21d09-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-133">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-135">Квалификаторы: **вмидатаид** (13)</span><span class="sxs-lookup"><span data-stu-id="21d09-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-136">Второй IP-адрес сервера, используемый для запросов DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="21d09-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="21d09-137">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-138">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="21d09-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-140">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-142">Квалификаторы: **вмидатаид** (14)</span><span class="sxs-lookup"><span data-stu-id="21d09-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-143">Третий IP-адрес сервера, используемый для запросов DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="21d09-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="21d09-144">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-145">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="21d09-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-149">Квалификаторы: **вмидатаид** (15)</span><span class="sxs-lookup"><span data-stu-id="21d09-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-150">Четвертый IP-адрес сервера, используемый для запросов DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="21d09-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="21d09-151">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-152">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-153">**Шлюз**</span><span class="sxs-lookup"><span data-stu-id="21d09-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-154">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-156">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="21d09-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-157">IP-адрес шлюза по умолчанию, используемого компьютерной системой.</span><span class="sxs-lookup"><span data-stu-id="21d09-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="21d09-158">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-159">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="21d09-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21d09-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-163">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="21d09-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-164">Индекс адаптера.</span><span class="sxs-lookup"><span data-stu-id="21d09-164">Adapter index.</span></span> <span data-ttu-id="21d09-165">Индекс адаптера может измениться, если адаптер отключен, а затем включен или в других обстоятельствах и не должен считаться постоянным.</span><span class="sxs-lookup"><span data-stu-id="21d09-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-166">**IP**</span><span class="sxs-lookup"><span data-stu-id="21d09-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-167">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-169">Квалификаторы: **вмидатаид** (6)</span><span class="sxs-lookup"><span data-stu-id="21d09-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-170">IP-адреса, связанные с сетевой картой.</span><span class="sxs-lookup"><span data-stu-id="21d09-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="21d09-171">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-172">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-173">**NICName**</span><span class="sxs-lookup"><span data-stu-id="21d09-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-174">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="21d09-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="21d09-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-176">Квалификаторы: **вмидатаид** (1), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="21d09-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-177">Имя сетевой карты.</span><span class="sxs-lookup"><span data-stu-id="21d09-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-178">**фисикаладдр**</span><span class="sxs-lookup"><span data-stu-id="21d09-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-179">Тип данных: **Char16**</span><span class="sxs-lookup"><span data-stu-id="21d09-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-181">Квалификаторы: **вмидатаид** (4), **Max** (8)</span><span class="sxs-lookup"><span data-stu-id="21d09-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-182">Аппаратный адрес для адаптера.</span><span class="sxs-lookup"><span data-stu-id="21d09-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-183">**фисикаладдрлен**</span><span class="sxs-lookup"><span data-stu-id="21d09-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-184">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21d09-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-186">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="21d09-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-187">Длина аппаратного адреса адаптера.</span><span class="sxs-lookup"><span data-stu-id="21d09-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-188">**примаривинссервер**</span><span class="sxs-lookup"><span data-stu-id="21d09-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-189">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-191">Квалификаторы: **вмидатаид** (10)</span><span class="sxs-lookup"><span data-stu-id="21d09-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-192">IP-адрес основного WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="21d09-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="21d09-193">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-194">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-195">**секондаривинссервер**</span><span class="sxs-lookup"><span data-stu-id="21d09-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-196">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-198">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="21d09-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-199">IP-адрес дополнительного WINS-сервера.</span><span class="sxs-lookup"><span data-stu-id="21d09-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="21d09-200">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-201">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-202">**Размер**</span><span class="sxs-lookup"><span data-stu-id="21d09-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21d09-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-205">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="21d09-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-206">Размер (в байтах) свойства данных.</span><span class="sxs-lookup"><span data-stu-id="21d09-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="21d09-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="21d09-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21d09-208">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="21d09-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="21d09-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21d09-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21d09-210">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="21d09-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="21d09-211">Маска подсети, связанная с сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="21d09-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="21d09-212">Каждый байт Sint32 представляет одну из четырех частей IP-адреса (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="21d09-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="21d09-213">Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="21d09-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21d09-214">Требования</span><span class="sxs-lookup"><span data-stu-id="21d09-214">Requirements</span></span>



| <span data-ttu-id="21d09-215">Требование</span><span class="sxs-lookup"><span data-stu-id="21d09-215">Requirement</span></span> | <span data-ttu-id="21d09-216">Значение</span><span class="sxs-lookup"><span data-stu-id="21d09-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="21d09-217">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21d09-217">Minimum supported client</span></span><br/> | <span data-ttu-id="21d09-218">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="21d09-218">None supported</span></span><br/>                            |
| <span data-ttu-id="21d09-219">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21d09-219">Minimum supported server</span></span><br/> | <span data-ttu-id="21d09-220">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21d09-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21d09-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21d09-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d09-222">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="21d09-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




