---
description: Представляет связь между экземпляром Мсвм \_ ComputerSystem, представляющей виртуальную машину, и экземпляром мсвм \_ репликатионрелатионшип, который представляет отношение репликации виртуальной машины.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Класс Msvm_SystemReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990931"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="2b917-103">\_Класс мсвм системрепликатионрелатионшип</span><span class="sxs-lookup"><span data-stu-id="2b917-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="2b917-104">Представляет связь между экземпляром [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющей виртуальную машину, и экземпляром [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , который представляет отношение репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b917-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="2b917-105">Этот класс является производным от [**класса \_ зависимостей CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="2b917-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="2b917-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2b917-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b917-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b917-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2b917-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2b917-108">Members</span></span>

<span data-ttu-id="2b917-109">Класс **мсвм \_ системрепликатионрелатионшип** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b917-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="2b917-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b917-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b917-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b917-111">Properties</span></span>

<span data-ttu-id="2b917-112">Класс **мсвм \_ системрепликатионрелатионшип** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b917-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b917-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2b917-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b917-114">Тип данных: **мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="2b917-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2b917-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b917-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b917-116">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2b917-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2b917-117">Ссылка на экземпляр класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющий виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2b917-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2b917-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="2b917-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b917-119">Тип данных: **мсвм \_ репликатионрелатионшип**</span><span class="sxs-lookup"><span data-stu-id="2b917-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="2b917-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b917-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b917-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")</span><span class="sxs-lookup"><span data-stu-id="2b917-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2b917-122">Ссылка на экземпляр класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , представляющий отношение репликации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="2b917-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b917-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2b917-123">Requirements</span></span>



| <span data-ttu-id="2b917-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2b917-124">Requirement</span></span> | <span data-ttu-id="2b917-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2b917-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b917-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b917-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2b917-127">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b917-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2b917-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b917-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2b917-129">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b917-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2b917-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b917-130">Namespace</span></span><br/>                | <span data-ttu-id="2b917-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2b917-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2b917-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2b917-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b917-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b917-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b917-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2b917-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b917-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b917-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b917-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b917-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b917-137">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="2b917-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="2b917-138">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="2b917-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

