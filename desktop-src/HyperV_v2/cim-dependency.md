---
description: Представляет универсальную ассоциацию, используемую для установления отношений зависимости между управляемыми элементами.
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: Класс CIM_Dependency (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662604"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="b0d89-103">Класс CIM_Dependency (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b0d89-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="b0d89-104">Представляет универсальную ассоциацию, используемую для установления отношений зависимости между управляемыми элементами.</span><span class="sxs-lookup"><span data-stu-id="b0d89-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d89-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0d89-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b0d89-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b0d89-106">Members</span></span>

<span data-ttu-id="b0d89-107">Класс **\_ зависимостей CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b0d89-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="b0d89-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0d89-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0d89-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="b0d89-109">Properties</span></span>

<span data-ttu-id="b0d89-110">Класс **\_ зависимости CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="b0d89-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0d89-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="b0d89-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d89-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="b0d89-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="b0d89-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0d89-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0d89-114">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b0d89-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b0d89-115">Независимый объект в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="b0d89-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="b0d89-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="b0d89-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d89-117">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="b0d89-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="b0d89-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0d89-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0d89-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b0d89-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b0d89-120">Зависимый объект в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="b0d89-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0d89-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b0d89-121">Requirements</span></span>



| <span data-ttu-id="b0d89-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b0d89-122">Requirement</span></span> | <span data-ttu-id="b0d89-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b0d89-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d89-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0d89-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d89-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b0d89-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b0d89-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0d89-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d89-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0d89-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b0d89-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0d89-128">Namespace</span></span><br/>                | <span data-ttu-id="b0d89-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b0d89-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b0d89-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b0d89-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0d89-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0d89-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0d89-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b0d89-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0d89-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0d89-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

