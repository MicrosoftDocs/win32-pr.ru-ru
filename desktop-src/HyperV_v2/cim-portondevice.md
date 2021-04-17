---
description: Представляет связь между портом или точкой подключения и устройством.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: Класс CIM_PortOnDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664775"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="15575-103">\_Класс CIM портондевице</span><span class="sxs-lookup"><span data-stu-id="15575-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="15575-104">Представляет связь между портом или точкой подключения и устройством.</span><span class="sxs-lookup"><span data-stu-id="15575-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="15575-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15575-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="15575-106">Члены</span><span class="sxs-lookup"><span data-stu-id="15575-106">Members</span></span>

<span data-ttu-id="15575-107">Класс **CIM \_ портондевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="15575-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="15575-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="15575-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15575-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="15575-109">Properties</span></span>

<span data-ttu-id="15575-110">Класс **CIM \_ портондевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15575-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15575-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="15575-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15575-112">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="15575-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="15575-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15575-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15575-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="15575-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="15575-115">Устройство, содержащее порт.</span><span class="sxs-lookup"><span data-stu-id="15575-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="15575-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="15575-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15575-117">Тип данных: **CIM \_ логикалпорт**</span><span class="sxs-lookup"><span data-stu-id="15575-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="15575-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15575-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15575-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="15575-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="15575-120">Порт на устройстве.</span><span class="sxs-lookup"><span data-stu-id="15575-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15575-121">Требования</span><span class="sxs-lookup"><span data-stu-id="15575-121">Requirements</span></span>



| <span data-ttu-id="15575-122">Требование</span><span class="sxs-lookup"><span data-stu-id="15575-122">Requirement</span></span> | <span data-ttu-id="15575-123">Значение</span><span class="sxs-lookup"><span data-stu-id="15575-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15575-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15575-124">Minimum supported client</span></span><br/> | <span data-ttu-id="15575-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15575-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15575-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15575-126">Minimum supported server</span></span><br/> | <span data-ttu-id="15575-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15575-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15575-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="15575-128">Namespace</span></span><br/>                | <span data-ttu-id="15575-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="15575-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15575-130">MOF</span><span class="sxs-lookup"><span data-stu-id="15575-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15575-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15575-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15575-132">DLL</span><span class="sxs-lookup"><span data-stu-id="15575-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15575-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15575-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15575-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15575-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15575-135">**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="15575-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

