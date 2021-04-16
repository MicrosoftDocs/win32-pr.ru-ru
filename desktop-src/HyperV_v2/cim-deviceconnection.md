---
description: Связь, указывающая, что два или несколько устройств соединяются друг с другом.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: Класс CIM_DeviceConnection (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682947"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="1f179-103">Класс CIM_DeviceConnection (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="1f179-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="1f179-104">Связь, указывающая, что два или несколько устройств соединяются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="1f179-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f179-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f179-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="1f179-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1f179-106">Members</span></span>

<span data-ttu-id="1f179-107">Класс **CIM \_ девицеконнектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1f179-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="1f179-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f179-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f179-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f179-109">Properties</span></span>

<span data-ttu-id="1f179-110">Класс **CIM \_ девицеконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f179-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f179-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="1f179-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f179-112">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="1f179-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1f179-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f179-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f179-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1f179-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1f179-115">устройству;</span><span class="sxs-lookup"><span data-stu-id="1f179-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="1f179-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="1f179-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f179-117">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="1f179-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1f179-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f179-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f179-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="1f179-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1f179-120">Второе устройство, подключенное к другому устройству.</span><span class="sxs-lookup"><span data-stu-id="1f179-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="1f179-121">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="1f179-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f179-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f179-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f179-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f179-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f179-124">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Связь портов шины DMTF \| 001,3 "), **Пунит** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="1f179-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="1f179-125">Если возможны несколько значений ширины данных шины и соединения, свойство Неготиатеддатавидс определяет ту, которая используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="1f179-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="1f179-126">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="1f179-126">Data width is specified in bits.</span></span> <span data-ttu-id="1f179-127">Если ширина данных не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="1f179-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1f179-128">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="1f179-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f179-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f179-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f179-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1f179-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f179-131">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Связь портов шины DMTF \| 001,2 "), **Пунит** (" бит/сек ")</span><span class="sxs-lookup"><span data-stu-id="1f179-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="1f179-132">Если возможны несколько скоростей шины и соединения, это свойство определяет скорость, используемую между устройствами, в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="1f179-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="1f179-133">Если скорость подключения или шины не согласована, или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение "0".</span><span class="sxs-lookup"><span data-stu-id="1f179-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f179-134">Требования</span><span class="sxs-lookup"><span data-stu-id="1f179-134">Requirements</span></span>



| <span data-ttu-id="1f179-135">Требование</span><span class="sxs-lookup"><span data-stu-id="1f179-135">Requirement</span></span> | <span data-ttu-id="1f179-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1f179-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f179-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f179-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1f179-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1f179-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1f179-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f179-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1f179-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f179-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1f179-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1f179-141">Namespace</span></span><br/>                | <span data-ttu-id="1f179-142">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1f179-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1f179-143">MOF</span><span class="sxs-lookup"><span data-stu-id="1f179-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f179-144"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f179-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f179-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1f179-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f179-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f179-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f179-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f179-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f179-148">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="1f179-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

