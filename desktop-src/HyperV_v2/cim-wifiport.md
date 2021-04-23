---
description: Представляет устройство связи для беспроводной локальной сети, которое соответствует серии спецификаций IEEE 802,11.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: Класс CIM_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910396"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="3b32d-103">\_Класс CIM вифипорт</span><span class="sxs-lookup"><span data-stu-id="3b32d-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="3b32d-104">Представляет устройство связи для беспроводной локальной сети, которое соответствует серии спецификаций IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="3b32d-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b32d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b32d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="3b32d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3b32d-106">Members</span></span>

<span data-ttu-id="3b32d-107">Класс **CIM \_ вифипорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3b32d-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="3b32d-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b32d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b32d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b32d-109">Properties</span></span>

<span data-ttu-id="3b32d-110">Класс **CIM \_ вифипорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3b32d-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b32d-111">**максспид**</span><span class="sxs-lookup"><span data-stu-id="3b32d-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b32d-112">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b32d-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("максспид")</span><span class="sxs-lookup"><span data-stu-id="3b32d-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="3b32d-115">Максимальная поддерживаемая пропускная способность (в битах в секунду) на основе режима работы, указанного в свойстве **portType** .</span><span class="sxs-lookup"><span data-stu-id="3b32d-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="3b32d-116">Например, **максспид** имеет значение "11000000", если **PortType** содержит "71" (802.11 b).</span><span class="sxs-lookup"><span data-stu-id="3b32d-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="3b32d-117">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="3b32d-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b32d-118">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3b32d-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="3b32d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="3b32d-121">Массив, содержащий MAC-адреса в стандарте IEEE 802 EUI-48.</span><span class="sxs-lookup"><span data-stu-id="3b32d-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="3b32d-122">MAC-адрес имеет формат, состоящий из двенадцати шестнадцатеричных цифр, каждая из которых представляет один из шести октетов MAC-адреса в каноническом порядке.</span><span class="sxs-lookup"><span data-stu-id="3b32d-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="3b32d-123">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="3b32d-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b32d-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b32d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("перманентаддресс")</span><span class="sxs-lookup"><span data-stu-id="3b32d-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="3b32d-127">MAC-адрес порта IEEE 802 EUI-48.</span><span class="sxs-lookup"><span data-stu-id="3b32d-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="3b32d-128">MAC-адрес имеет формат, состоящий из двенадцати шестнадцатеричных цифр, каждая из которых представляет один из шести октетов MAC-адреса в каноническом порядке.</span><span class="sxs-lookup"><span data-stu-id="3b32d-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="3b32d-129">**Порта**</span><span class="sxs-lookup"><span data-stu-id="3b32d-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b32d-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b32d-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="3b32d-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="3b32d-133">Режим работы 802,11, включенный для порта.</span><span class="sxs-lookup"><span data-stu-id="3b32d-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b32d-134">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3b32d-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b32d-135">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3b32d-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="3b32d-136">**802.11 a** (70)</span><span class="sxs-lookup"><span data-stu-id="3b32d-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="3b32d-137">**802.11 b** (71)</span><span class="sxs-lookup"><span data-stu-id="3b32d-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="3b32d-138">**802.11 g** (72)</span><span class="sxs-lookup"><span data-stu-id="3b32d-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="3b32d-139">**802.11 n** (73)</span><span class="sxs-lookup"><span data-stu-id="3b32d-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3b32d-140">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3b32d-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3b32d-141">**Поставщик зарезервирован** (16000...)</span><span class="sxs-lookup"><span data-stu-id="3b32d-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b32d-142">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="3b32d-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b32d-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b32d-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b32d-145">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("скорость")</span><span class="sxs-lookup"><span data-stu-id="3b32d-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="3b32d-146">Скорость передачи данных, с которой была получена текущая единица данных протокола ППДУ (ПЛКП (протокол конвергенции физических уровней), в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="3b32d-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="3b32d-147">Это значение кодируется в первых 4 битах заголовка ПЛКП в каждом кадре ПЛКП.</span><span class="sxs-lookup"><span data-stu-id="3b32d-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b32d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="3b32d-148">Requirements</span></span>



| <span data-ttu-id="3b32d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="3b32d-149">Requirement</span></span> | <span data-ttu-id="3b32d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="3b32d-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b32d-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b32d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3b32d-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3b32d-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3b32d-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b32d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3b32d-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b32d-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3b32d-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b32d-155">Namespace</span></span><br/>                | <span data-ttu-id="3b32d-156">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3b32d-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3b32d-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3b32d-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b32d-158"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b32d-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b32d-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3b32d-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b32d-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b32d-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b32d-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b32d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b32d-162">**\_НЕТВОРКПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="3b32d-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

