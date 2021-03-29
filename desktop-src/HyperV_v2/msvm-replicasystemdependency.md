---
description: Представляет связь между экземпляром \_ класса COMPUTERSYSTEM CIM, представляющего реплику виртуальной машины, и экземпляром класса платформы CIM \_ , представляющего тестовую реплику виртуальной машины.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Класс Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264721"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="6ee95-103">\_Класс мсвм репликасистемдепенденци</span><span class="sxs-lookup"><span data-stu-id="6ee95-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="6ee95-104">Представляет связь между экземпляром класса [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющего реплику виртуальной машины, и экземпляром класса платформы **CIM, \_** представляющего тестовую реплику виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6ee95-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="6ee95-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6ee95-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee95-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ee95-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6ee95-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6ee95-107">Members</span></span>

<span data-ttu-id="6ee95-108">Класс **мсвм \_ репликасистемдепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ee95-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="6ee95-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ee95-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ee95-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ee95-110">Properties</span></span>

<span data-ttu-id="6ee95-111">Класс **мсвм \_ репликасистемдепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6ee95-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ee95-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="6ee95-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee95-113">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6ee95-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ee95-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-115">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6ee95-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6ee95-116">Ссылка на экземпляр класса [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий реплику виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6ee95-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="6ee95-117">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="6ee95-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="6ee95-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="6ee95-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ee95-119">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6ee95-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ee95-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ зависимость CIM. Dependent")</span><span class="sxs-lookup"><span data-stu-id="6ee95-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6ee95-122">Ссылка на экземпляр класса [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий тестовую реплику виртуальной машины, созданную методом [**мсвм \_ репликатионсервице. тестрепликасистем**](testreplicasystem-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="6ee95-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="6ee95-123">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="6ee95-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ee95-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6ee95-124">Requirements</span></span>



| <span data-ttu-id="6ee95-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6ee95-125">Requirement</span></span> | <span data-ttu-id="6ee95-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6ee95-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee95-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ee95-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee95-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6ee95-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ee95-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ee95-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee95-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6ee95-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ee95-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6ee95-131">Namespace</span></span><br/>                | <span data-ttu-id="6ee95-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6ee95-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ee95-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6ee95-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ee95-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ee95-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ee95-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee95-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee95-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ee95-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

