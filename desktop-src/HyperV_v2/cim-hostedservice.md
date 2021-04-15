---
description: Представляет связь между службой и системой, в которой размещена служба. В системе может размещаться много служб, однако этот класс не представляет службы, размещенные в нескольких системах.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: Класс CIM_HostedService (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496908"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="53b4f-104">Класс CIM_HostedService (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="53b4f-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="53b4f-105">Представляет связь между службой и системой, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="53b4f-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="53b4f-106">В системе может размещаться много служб, однако этот класс не представляет службы, размещенные в нескольких системах.</span><span class="sxs-lookup"><span data-stu-id="53b4f-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b4f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53b4f-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="53b4f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="53b4f-108">Members</span></span>

<span data-ttu-id="53b4f-109">Класс **CIM \_ HostedService** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="53b4f-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="53b4f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="53b4f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53b4f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="53b4f-111">Properties</span></span>

<span data-ttu-id="53b4f-112">Класс **CIM \_ HostedService** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="53b4f-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53b4f-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="53b4f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53b4f-114">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="53b4f-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="53b4f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53b4f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53b4f-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="53b4f-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="53b4f-117">Система размещения.</span><span class="sxs-lookup"><span data-stu-id="53b4f-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="53b4f-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="53b4f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53b4f-119">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="53b4f-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="53b4f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="53b4f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53b4f-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="53b4f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="53b4f-122">Служба, размещенная в системе.</span><span class="sxs-lookup"><span data-stu-id="53b4f-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53b4f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="53b4f-123">Requirements</span></span>



| <span data-ttu-id="53b4f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="53b4f-124">Requirement</span></span> | <span data-ttu-id="53b4f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="53b4f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53b4f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53b4f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="53b4f-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="53b4f-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="53b4f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53b4f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="53b4f-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53b4f-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="53b4f-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="53b4f-130">Namespace</span></span><br/>                | <span data-ttu-id="53b4f-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="53b4f-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53b4f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="53b4f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53b4f-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53b4f-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53b4f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="53b4f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53b4f-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53b4f-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53b4f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53b4f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b4f-137">**\_ХОСТЕДДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="53b4f-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

