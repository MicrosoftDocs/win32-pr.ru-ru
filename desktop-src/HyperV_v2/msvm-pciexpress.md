---
description: Представляет состояние порта PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Класс Msvm_PciExpress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684462"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="981ab-103">\_Класс мсвм пЦиекспресс</span><span class="sxs-lookup"><span data-stu-id="981ab-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="981ab-104">Представляет состояние порта PCI Express.</span><span class="sxs-lookup"><span data-stu-id="981ab-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="981ab-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="981ab-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="981ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="981ab-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="981ab-107">Члены</span><span class="sxs-lookup"><span data-stu-id="981ab-107">Members</span></span>

<span data-ttu-id="981ab-108">Класс **мсвм \_ пЦиекспресс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="981ab-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="981ab-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="981ab-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="981ab-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="981ab-110">Properties</span></span>

<span data-ttu-id="981ab-111">Класс **мсвм \_ пЦиекспресс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="981ab-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="981ab-112">**девицеинстанцепас**</span><span class="sxs-lookup"><span data-stu-id="981ab-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ab-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="981ab-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="981ab-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="981ab-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="981ab-115">Строка, содержащая путь к экземпляру устройства, который определяет виртуальное устройство PCI Express.</span><span class="sxs-lookup"><span data-stu-id="981ab-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="981ab-116">**функтионнумбер**</span><span class="sxs-lookup"><span data-stu-id="981ab-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ab-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="981ab-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="981ab-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="981ab-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="981ab-119">Номер функции виртуального устройства PCI Express.</span><span class="sxs-lookup"><span data-stu-id="981ab-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="981ab-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="981ab-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="981ab-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="981ab-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="981ab-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="981ab-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="981ab-123">Строка, содержащая путь расположения устройства, который определяет виртуальное устройство PCI Express.</span><span class="sxs-lookup"><span data-stu-id="981ab-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="981ab-124">Требования</span><span class="sxs-lookup"><span data-stu-id="981ab-124">Requirements</span></span>



| <span data-ttu-id="981ab-125">Требование</span><span class="sxs-lookup"><span data-stu-id="981ab-125">Requirement</span></span> | <span data-ttu-id="981ab-126">Значение</span><span class="sxs-lookup"><span data-stu-id="981ab-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="981ab-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="981ab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="981ab-128">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="981ab-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="981ab-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="981ab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="981ab-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="981ab-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="981ab-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="981ab-131">Namespace</span></span><br/>                | <span data-ttu-id="981ab-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="981ab-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="981ab-133">MOF</span><span class="sxs-lookup"><span data-stu-id="981ab-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="981ab-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="981ab-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="981ab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="981ab-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="981ab-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="981ab-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="981ab-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="981ab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981ab-138">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="981ab-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




