---
description: Представляет конфигурацию сетевого адаптера в гостевой операционной системе.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Класс Msvm_GuestNetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154595"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="977a3-103">\_Класс мсвм гуестнетворкадаптерконфигуратион</span><span class="sxs-lookup"><span data-stu-id="977a3-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="977a3-104">Представляет конфигурацию сетевого адаптера в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="977a3-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="977a3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="977a3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="977a3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="977a3-107">Члены</span><span class="sxs-lookup"><span data-stu-id="977a3-107">Members</span></span>

<span data-ttu-id="977a3-108">Класс **мсвм \_ гуестнетворкадаптерконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="977a3-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="977a3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="977a3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="977a3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="977a3-110">Properties</span></span>

<span data-ttu-id="977a3-111">Класс **мсвм \_ гуестнетворкадаптерконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="977a3-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="977a3-112">**дефаултгатевайс**</span><span class="sxs-lookup"><span data-stu-id="977a3-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="977a3-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="977a3-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="977a3-115">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="977a3-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="977a3-116">Массив строк, содержащий IP-шлюзы по умолчанию, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="977a3-117">Максимальное число IP-шлюзов по умолчанию, которые могут быть настроены на одном сетевом адаптере, составляет пять.</span><span class="sxs-lookup"><span data-stu-id="977a3-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="977a3-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="977a3-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="977a3-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="977a3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="977a3-121">Указывает, включена ли DHCP на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="977a3-122">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="977a3-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-123">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="977a3-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="977a3-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="977a3-125">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="977a3-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="977a3-126">Массив строк, содержащий DNS-серверы, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="977a3-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="977a3-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="977a3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="977a3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="977a3-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="977a3-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="977a3-131">Уникальный идентификатор для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="977a3-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="977a3-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="977a3-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="977a3-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="977a3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="977a3-135">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="977a3-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="977a3-136">Массив строк, содержащий IP-адреса, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="977a3-137">**ипаддрессоригинс**</span><span class="sxs-lookup"><span data-stu-id="977a3-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-138">Тип данных: **UINT16** , массив</span><span class="sxs-lookup"><span data-stu-id="977a3-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="977a3-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="977a3-140">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="977a3-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="977a3-141">Источник IP-адресов, настроенных на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="977a3-142">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="977a3-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="977a3-143">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="977a3-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="977a3-144">**Статический** (2)</span><span class="sxs-lookup"><span data-stu-id="977a3-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="977a3-145">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="977a3-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="977a3-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="977a3-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="977a3-148">Определяет IP-протоколы, к которым применяются параметры, заданные этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="977a3-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="977a3-149">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="977a3-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="977a3-150">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="977a3-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="977a3-151">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="977a3-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="977a3-152">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="977a3-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="977a3-153">**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="977a3-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="977a3-154">**Подсети**</span><span class="sxs-lookup"><span data-stu-id="977a3-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977a3-155">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="977a3-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="977a3-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="977a3-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="977a3-157">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="977a3-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="977a3-158">Массив строк, содержащий подсети, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="977a3-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="977a3-159">Каждый элемент в этом массиве применяется к соответствующему элементу в массиве **ipaddresses** .</span><span class="sxs-lookup"><span data-stu-id="977a3-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="977a3-160">Требования</span><span class="sxs-lookup"><span data-stu-id="977a3-160">Requirements</span></span>



| <span data-ttu-id="977a3-161">Требование</span><span class="sxs-lookup"><span data-stu-id="977a3-161">Requirement</span></span> | <span data-ttu-id="977a3-162">Значение</span><span class="sxs-lookup"><span data-stu-id="977a3-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="977a3-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="977a3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="977a3-164">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="977a3-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="977a3-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="977a3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="977a3-166">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="977a3-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="977a3-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="977a3-167">Namespace</span></span><br/>                | <span data-ttu-id="977a3-168">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="977a3-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="977a3-169">MOF</span><span class="sxs-lookup"><span data-stu-id="977a3-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="977a3-170"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="977a3-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="977a3-171">DLL</span><span class="sxs-lookup"><span data-stu-id="977a3-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="977a3-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="977a3-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

