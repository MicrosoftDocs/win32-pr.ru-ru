---
description: Представляет связь между точкой доступа к службе (SAP) и логическим устройством, которое ее реализует.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Класс CIM_DeviceSAPImplementation (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682946"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="4b363-103">Класс CIM_DeviceSAPImplementation (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4b363-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="4b363-104">Представляет связь между точкой доступа к службе (SAP) и логическим устройством, которое ее реализует.</span><span class="sxs-lookup"><span data-stu-id="4b363-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b363-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b363-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4b363-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4b363-106">Members</span></span>

<span data-ttu-id="4b363-107">Класс **CIM \_ девицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b363-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="4b363-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b363-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b363-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b363-109">Properties</span></span>

<span data-ttu-id="4b363-110">Класс **CIM \_ девицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b363-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b363-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4b363-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b363-112">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="4b363-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4b363-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b363-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b363-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4b363-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4b363-115">Логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="4b363-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="4b363-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="4b363-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b363-117">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="4b363-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="4b363-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b363-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b363-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4b363-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4b363-120">Протокол SAP, реализованный логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="4b363-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b363-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4b363-121">Requirements</span></span>



| <span data-ttu-id="4b363-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4b363-122">Requirement</span></span> | <span data-ttu-id="4b363-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4b363-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b363-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b363-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b363-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4b363-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4b363-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b363-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b363-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b363-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4b363-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b363-128">Namespace</span></span><br/>                | <span data-ttu-id="4b363-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4b363-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b363-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4b363-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b363-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b363-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b363-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4b363-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b363-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b363-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b363-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b363-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b363-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="4b363-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

