---
description: Представляет порт Ethernet.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: Класс CIM_EthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539922"
---
# <a name="cim_ethernetport-class"></a><span data-ttu-id="e9ff1-103">\_Класс CIM есернетпорт</span><span class="sxs-lookup"><span data-stu-id="e9ff1-103">CIM\_EthernetPort class</span></span>

<span data-ttu-id="e9ff1-104">Представляет порт Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-104">Represents an ethernet port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ff1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9ff1-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="e9ff1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e9ff1-106">Members</span></span>

<span data-ttu-id="e9ff1-107">Класс **CIM \_ есернетпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e9ff1-107">The **CIM\_EthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="e9ff1-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9ff1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9ff1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="e9ff1-109">Properties</span></span>

<span data-ttu-id="e9ff1-110">Класс **CIM \_ есернетпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-110">The **CIM\_EthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9ff1-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-112">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e9ff1-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-114">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ есернетпорт**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-115">Возможности порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-115">The capabilities of the ethernet port.</span></span>

> [!Note]  
> <span data-ttu-id="e9ff1-116">Если включены возможности отработки отказа или балансировки нагрузки, также необходимо определить объект [**CIM \_ спареграуп**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (отработка отказа) или [**CIM \_ екстракапаЦитиграуп**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (Балансировка нагрузки), чтобы полностью описать эту возможность.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-116">If failover or load balancing capabilities are enabled, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) object should also be defined to completely describe the capability.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9ff1-117">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9ff1-118">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-118">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="e9ff1-119">**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-119">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="e9ff1-120">**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-120">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="e9ff1-121">**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-121">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="e9ff1-122">**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-122">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9ff1-123">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-123">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-124">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-126">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ есернетпорт**.**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-127">Массив строк произвольной формы, содержащий более подробные пояснения для всех функций, указанных в массиве Capabilities.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-127">An array of free-form strings that provides more detailed explanations for any of the features that are indicated in the Capabilities array.</span></span> <span data-ttu-id="e9ff1-128">Элементы в этом массиве соответствуют элементам в массиве Capabilities.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-128">The items in this array correspond to the items in the Capabilities array.</span></span>

</dd> <dt>

<span data-ttu-id="e9ff1-129">**енабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-129">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-130">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e9ff1-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-132">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ есернетпорт**.**Возможности**","**CIM \_ есернетпорт**.**Осеренабледкапабилитиес**")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-132">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**", "**CIM\_EthernetPort**.**OtherEnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-133">Указывает, какие возможности включены в массиве Capabilities.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-133">Indicates which capabilities are enabled in the Capabilities array.</span></span> <span data-ttu-id="e9ff1-134">Элементы в этом массиве соответствуют элементам в массиве Capabilities.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-134">The items in this array correspond to the items in the Capabilities array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9ff1-135">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9ff1-136">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="e9ff1-137">**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-137">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="e9ff1-138">**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-138">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="e9ff1-139">**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-139">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="e9ff1-140">**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-140">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9ff1-141">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-141">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpPortMaxInfo ")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpPortMaxInfo")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-145">Максимальный размер поля сведений (не MAC), которое будет получено или передано.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-145">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="e9ff1-146">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-146">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-147">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-149">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-149">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-150">Сетевые адреса, назначенные порту.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-150">The network addresses assigned to the port.</span></span> <span data-ttu-id="e9ff1-151">Адрес — это 802,3 MAC, который имеет формат двенадцати шестнадцатеричных цифр (например, "010203040506"), где каждая пара цифр представляет один из шести октетов MAC-адреса в каноническом порядке.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-151">The address is a 802.3 MAC that is formatted as twelve hexadecimal digits (for example, "010203040506"), where each pair of digits represents one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="e9ff1-152">**осеренабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-152">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-153">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-155">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ есернетпорт**.**Енабледкапабилитиес**")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-155">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**EnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-156">Массив строк произвольной формы, которые предоставляют более подробные пояснения для любых элементов массива **енабледкапабилитиес** , для которых задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e9ff1-156">An array of free-form strings that provide more detailed explanations for any of the **EnabledCapabilities** array items that are set to 1 (Other).</span></span> <span data-ttu-id="e9ff1-157">Элементы в этом массиве соответствуют элементам массива **енабледкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="e9ff1-157">The items in this array correspond to the items in the **EnabledCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="e9ff1-158">**Порта**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-158">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9ff1-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e9ff1-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9ff1-161">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="e9ff1-161">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="e9ff1-162">Режим, включенный для порта.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-162">The mode that is enabled on the port.</span></span> <span data-ttu-id="e9ff1-163">Если задано значение 1 (другое), свойство **осерпорттипе** описывает режим.</span><span class="sxs-lookup"><span data-stu-id="e9ff1-163">When set to 1 (Other), the **OtherPortType** property describes the mode.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9ff1-164">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e9ff1-165">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

<span data-ttu-id="e9ff1-166">**переданный (50** )</span><span class="sxs-lookup"><span data-stu-id="e9ff1-166">**10BaseT** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

<span data-ttu-id="e9ff1-167">**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-167">**10-100BaseT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

<span data-ttu-id="e9ff1-168">**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-168">**100BaseT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

<span data-ttu-id="e9ff1-169">**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-169">**1000BaseT** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

<span data-ttu-id="e9ff1-170">**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-170">**2500BaseT** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

<span data-ttu-id="e9ff1-171">**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-171">**10GBaseT** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

<span data-ttu-id="e9ff1-172">**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-172">**10GBase-CX4** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

<span data-ttu-id="e9ff1-173">**100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-173">**100Base-FX** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

<span data-ttu-id="e9ff1-174">**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-174">**100Base-SX** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

<span data-ttu-id="e9ff1-175">**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-175">**1000Base-SX** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

<span data-ttu-id="e9ff1-176">**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-176">**1000Base-LX** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

<span data-ttu-id="e9ff1-177">**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-177">**1000Base-CX** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

<span data-ttu-id="e9ff1-178">**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-178">**10GBase-SR** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

<span data-ttu-id="e9ff1-179">**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-179">**10GBase-SW** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

<span data-ttu-id="e9ff1-180">**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-180">**10GBase-LX4** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

<span data-ttu-id="e9ff1-181">**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-181">**10GBase-LR** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

<span data-ttu-id="e9ff1-182">**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-182">**10GBase-LW** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

<span data-ttu-id="e9ff1-183">**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-183">**10GBase-ER** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

<span data-ttu-id="e9ff1-184">**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-184">**10GBase-EW** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e9ff1-185">**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e9ff1-185">**Vendor Reserved** (16000..65535)</span></span>


<span data-ttu-id="e9ff1-186"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e9ff1-186"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e9ff1-187">Требования</span><span class="sxs-lookup"><span data-stu-id="e9ff1-187">Requirements</span></span>



| <span data-ttu-id="e9ff1-188">Требование</span><span class="sxs-lookup"><span data-stu-id="e9ff1-188">Requirement</span></span> | <span data-ttu-id="e9ff1-189">Значение</span><span class="sxs-lookup"><span data-stu-id="e9ff1-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ff1-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9ff1-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ff1-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9ff1-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e9ff1-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9ff1-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ff1-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9ff1-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e9ff1-194">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9ff1-194">Namespace</span></span><br/>                | <span data-ttu-id="e9ff1-195">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e9ff1-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e9ff1-196">MOF</span><span class="sxs-lookup"><span data-stu-id="e9ff1-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9ff1-197"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9ff1-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9ff1-198">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ff1-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ff1-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9ff1-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9ff1-200">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9ff1-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ff1-201">**\_НЕТВОРКПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="e9ff1-201">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

