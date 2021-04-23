---
description: Представляет связь между службой и точкой доступа к службе (SAP), которая предоставляет службу с функциональными возможностями.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: Класс CIM_ServiceSAPDependency (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663592"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="70634-103">Класс CIM_ServiceSAPDependency (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="70634-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="70634-104">Представляет связь между службой и точкой доступа к службе (SAP), которая предоставляет службу с функциональными возможностями.</span><span class="sxs-lookup"><span data-stu-id="70634-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="70634-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70634-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="70634-106">Члены</span><span class="sxs-lookup"><span data-stu-id="70634-106">Members</span></span>

<span data-ttu-id="70634-107">Класс **CIM \_ сервицесапдепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70634-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="70634-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="70634-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70634-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="70634-109">Properties</span></span>

<span data-ttu-id="70634-110">Класс **CIM \_ сервицесапдепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70634-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70634-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="70634-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70634-112">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="70634-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="70634-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70634-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70634-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="70634-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="70634-115">Необходимая точка доступа к службе.</span><span class="sxs-lookup"><span data-stu-id="70634-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="70634-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="70634-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70634-117">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="70634-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="70634-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="70634-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70634-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="70634-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="70634-120">Служба, зависящая от SAP.</span><span class="sxs-lookup"><span data-stu-id="70634-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70634-121">Требования</span><span class="sxs-lookup"><span data-stu-id="70634-121">Requirements</span></span>



| <span data-ttu-id="70634-122">Требование</span><span class="sxs-lookup"><span data-stu-id="70634-122">Requirement</span></span> | <span data-ttu-id="70634-123">Значение</span><span class="sxs-lookup"><span data-stu-id="70634-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70634-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70634-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70634-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="70634-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="70634-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70634-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70634-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="70634-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="70634-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70634-128">Namespace</span></span><br/>                | <span data-ttu-id="70634-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="70634-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="70634-130">MOF</span><span class="sxs-lookup"><span data-stu-id="70634-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70634-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70634-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70634-132">DLL</span><span class="sxs-lookup"><span data-stu-id="70634-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70634-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70634-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70634-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70634-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70634-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="70634-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

