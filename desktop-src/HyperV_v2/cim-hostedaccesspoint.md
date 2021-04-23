---
description: Представляет связь между точкой доступа службы (SAP) и системой, в которой она размещается.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: Класс CIM_HostedAccessPoint (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496911"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="7e3be-103">Класс CIM_HostedAccessPoint (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7e3be-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="7e3be-104">Представляет связь между точкой доступа службы (SAP) и системой, в которой она размещается.</span><span class="sxs-lookup"><span data-stu-id="7e3be-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="7e3be-105">В системе может размещаться несколько точек доступа.</span><span class="sxs-lookup"><span data-stu-id="7e3be-105">A system can host multiple access points.</span></span> <span data-ttu-id="7e3be-106">Если реализация SAP моделируется, она должна быть реализована устройством или программным обеспечением, которое является частью системы, в которой размещается SAP.</span><span class="sxs-lookup"><span data-stu-id="7e3be-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e3be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e3be-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7e3be-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7e3be-108">Members</span></span>

<span data-ttu-id="7e3be-109">Класс **CIM \_ хостедакцесспоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7e3be-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7e3be-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7e3be-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e3be-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7e3be-111">Properties</span></span>

<span data-ttu-id="7e3be-112">Класс **CIM \_ хостедакцесспоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7e3be-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e3be-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7e3be-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3be-114">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="7e3be-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="7e3be-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e3be-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e3be-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7e3be-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7e3be-117">Система размещения.</span><span class="sxs-lookup"><span data-stu-id="7e3be-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="7e3be-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="7e3be-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e3be-119">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="7e3be-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="7e3be-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7e3be-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e3be-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7e3be-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7e3be-122">SAPs, размещенные в системе.</span><span class="sxs-lookup"><span data-stu-id="7e3be-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e3be-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7e3be-123">Requirements</span></span>



| <span data-ttu-id="7e3be-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7e3be-124">Requirement</span></span> | <span data-ttu-id="7e3be-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3be-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e3be-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e3be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7e3be-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7e3be-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7e3be-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e3be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7e3be-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7e3be-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7e3be-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7e3be-130">Namespace</span></span><br/>                | <span data-ttu-id="7e3be-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7e3be-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e3be-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7e3be-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e3be-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e3be-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e3be-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7e3be-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e3be-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e3be-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e3be-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e3be-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e3be-137">**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="7e3be-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

