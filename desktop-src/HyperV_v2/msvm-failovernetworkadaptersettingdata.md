---
description: Представляет параметры сетевого адаптера в гостевой операционной системе, который будет применен во время отработки отказа.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Класс Msvm_FailoverNetworkAdapterSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662528"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="626f5-103">\_Класс мсвм фаиловернетворкадаптерсеттингдата</span><span class="sxs-lookup"><span data-stu-id="626f5-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="626f5-104">Представляет параметры сетевого адаптера в гостевой операционной системе, который будет применен во время отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="626f5-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="626f5-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="626f5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="626f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="626f5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="626f5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="626f5-107">Members</span></span>

<span data-ttu-id="626f5-108">Класс **мсвм \_ фаиловернетворкадаптерсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="626f5-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="626f5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="626f5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="626f5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="626f5-110">Properties</span></span>

<span data-ttu-id="626f5-111">Класс **мсвм \_ фаиловернетворкадаптерсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="626f5-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="626f5-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="626f5-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626f5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626f5-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626f5-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="626f5-115">A short description of the object.</span></span> <span data-ttu-id="626f5-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="626f5-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-117">**дефаултгатевайс**</span><span class="sxs-lookup"><span data-stu-id="626f5-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-118">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="626f5-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="626f5-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626f5-120">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="626f5-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="626f5-121">Массив строк, задающих IP-шлюзы по умолчанию, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="626f5-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="626f5-122">Максимальное число IP-шлюзов по умолчанию, которые могут быть настроены на одном сетевом адаптере, составляет пять.</span><span class="sxs-lookup"><span data-stu-id="626f5-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="626f5-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626f5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626f5-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626f5-126">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="626f5-126">A description of the object.</span></span> <span data-ttu-id="626f5-127">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="626f5-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="626f5-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="626f5-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="626f5-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626f5-131">Указывает, включена ли DHCP в интерфейсе IPv4 сетевого адаптера в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="626f5-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-132">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="626f5-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="626f5-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="626f5-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626f5-135">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="626f5-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="626f5-136">Массив строк, указывающий DNS-серверы, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="626f5-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="626f5-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626f5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626f5-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626f5-140">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="626f5-140">A display name for the object.</span></span> <span data-ttu-id="626f5-141">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="626f5-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="626f5-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626f5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626f5-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626f5-145">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="626f5-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="626f5-146">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="626f5-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="626f5-147">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="626f5-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="626f5-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-149">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="626f5-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="626f5-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626f5-151">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="626f5-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="626f5-152">Массив строк, задающих IP-адреса, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="626f5-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="626f5-153">**протоколифтипе**</span><span class="sxs-lookup"><span data-stu-id="626f5-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="626f5-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="626f5-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626f5-156">Определяет протоколы Интернета, к которым применяются параметры, заданные этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="626f5-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="626f5-157">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="626f5-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="626f5-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="626f5-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="626f5-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="626f5-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="626f5-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="626f5-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="626f5-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="626f5-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="626f5-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="626f5-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="626f5-163">IPv4 или IPv6</span><span class="sxs-lookup"><span data-stu-id="626f5-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="626f5-164">**Подсети**</span><span class="sxs-lookup"><span data-stu-id="626f5-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626f5-165">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="626f5-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="626f5-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626f5-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626f5-167">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="626f5-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="626f5-168">Массив строк, задающих подсети, настроенные на сетевом адаптере в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="626f5-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="626f5-169">Каждый элемент в этом массиве применяется к соответствующему элементу в массиве **ipaddresses** .</span><span class="sxs-lookup"><span data-stu-id="626f5-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="626f5-170">Требования</span><span class="sxs-lookup"><span data-stu-id="626f5-170">Requirements</span></span>



| <span data-ttu-id="626f5-171">Требование</span><span class="sxs-lookup"><span data-stu-id="626f5-171">Requirement</span></span> | <span data-ttu-id="626f5-172">Значение</span><span class="sxs-lookup"><span data-stu-id="626f5-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="626f5-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="626f5-173">Minimum supported client</span></span><br/> | <span data-ttu-id="626f5-174">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="626f5-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="626f5-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="626f5-175">Minimum supported server</span></span><br/> | <span data-ttu-id="626f5-176">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="626f5-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="626f5-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="626f5-177">Namespace</span></span><br/>                | <span data-ttu-id="626f5-178">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="626f5-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="626f5-179">MOF</span><span class="sxs-lookup"><span data-stu-id="626f5-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="626f5-180"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="626f5-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="626f5-181">DLL</span><span class="sxs-lookup"><span data-stu-id="626f5-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="626f5-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="626f5-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

