---
description: Ассоциация между экземпляром Мсвм \_ всскомпонент и экземпляром мсвм \_ всссервице, который представляет службу для выполнения операций с компонентом VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Класс Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683750"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="043df-103">\_Класс мсвм сервицеофвсскомпонент</span><span class="sxs-lookup"><span data-stu-id="043df-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="043df-104">Ассоциация между экземпляром [**мсвм \_ всскомпонент**](msvm-vsscomponent.md) и экземпляром [**мсвм \_ всссервице**](msvm-vssservice.md) , который представляет службу для выполнения операций с компонентом VSS.</span><span class="sxs-lookup"><span data-stu-id="043df-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="043df-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="043df-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="043df-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="043df-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="043df-107">Члены</span><span class="sxs-lookup"><span data-stu-id="043df-107">Members</span></span>

<span data-ttu-id="043df-108">Класс **мсвм \_ сервицеофвсскомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="043df-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="043df-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="043df-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="043df-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="043df-110">Properties</span></span>

<span data-ttu-id="043df-111">Класс **мсвм \_ сервицеофвсскомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="043df-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="043df-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="043df-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043df-113">Тип данных: **мсвм \_ всскомпонент**</span><span class="sxs-lookup"><span data-stu-id="043df-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="043df-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043df-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043df-115">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="043df-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="043df-116">A, [**мсвм \_ всскомпонент**](msvm-vsscomponent.md) , представляющий компонент VSS.</span><span class="sxs-lookup"><span data-stu-id="043df-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="043df-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="043df-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043df-118">Тип данных: **мсвм \_ всссервице**</span><span class="sxs-lookup"><span data-stu-id="043df-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="043df-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043df-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043df-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")</span><span class="sxs-lookup"><span data-stu-id="043df-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="043df-121">[**Мсвм \_ всссервице**](msvm-vssservice.md) , представляющий службу VSS IC.</span><span class="sxs-lookup"><span data-stu-id="043df-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="043df-122">Требования</span><span class="sxs-lookup"><span data-stu-id="043df-122">Requirements</span></span>



| <span data-ttu-id="043df-123">Требование</span><span class="sxs-lookup"><span data-stu-id="043df-123">Requirement</span></span> | <span data-ttu-id="043df-124">Значение</span><span class="sxs-lookup"><span data-stu-id="043df-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="043df-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="043df-125">Minimum supported client</span></span><br/> | <span data-ttu-id="043df-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="043df-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="043df-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="043df-127">Minimum supported server</span></span><br/> | <span data-ttu-id="043df-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="043df-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="043df-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="043df-129">Namespace</span></span><br/>                | <span data-ttu-id="043df-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="043df-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="043df-131">MOF</span><span class="sxs-lookup"><span data-stu-id="043df-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="043df-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="043df-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="043df-133">DLL</span><span class="sxs-lookup"><span data-stu-id="043df-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="043df-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="043df-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="043df-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="043df-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043df-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="043df-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

