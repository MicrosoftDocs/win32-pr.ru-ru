---
description: Представляет связь между системой и одним из элементов, составляющих ее.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: Класс CIM_SystemComponent (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908736"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="78630-103">Класс CIM_SystemComponent (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="78630-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="78630-104">Представляет связь между системой и одним из элементов, составляющих ее.</span><span class="sxs-lookup"><span data-stu-id="78630-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="78630-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78630-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="78630-106">Члены</span><span class="sxs-lookup"><span data-stu-id="78630-106">Members</span></span>

<span data-ttu-id="78630-107">Класс **CIM \_ системкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="78630-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="78630-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="78630-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78630-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="78630-109">Properties</span></span>

<span data-ttu-id="78630-110">Класс **CIM \_ системкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="78630-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78630-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="78630-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78630-112">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="78630-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="78630-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78630-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78630-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="78630-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="78630-115">[**\_ Система CIM**](cim-system.md) , содержащая объект **PartComponent**.</span><span class="sxs-lookup"><span data-stu-id="78630-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="78630-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="78630-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78630-117">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="78630-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="78630-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78630-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78630-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="78630-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="78630-120">Дочерняя [**\_ манажедсистемелемент CIM**](cim-managedsystemelement.md) , которая является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="78630-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78630-121">Требования</span><span class="sxs-lookup"><span data-stu-id="78630-121">Requirements</span></span>



| <span data-ttu-id="78630-122">Требование</span><span class="sxs-lookup"><span data-stu-id="78630-122">Requirement</span></span> | <span data-ttu-id="78630-123">Значение</span><span class="sxs-lookup"><span data-stu-id="78630-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78630-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78630-124">Minimum supported client</span></span><br/> | <span data-ttu-id="78630-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="78630-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="78630-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78630-126">Minimum supported server</span></span><br/> | <span data-ttu-id="78630-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78630-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="78630-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78630-128">Namespace</span></span><br/>                | <span data-ttu-id="78630-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="78630-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="78630-130">MOF</span><span class="sxs-lookup"><span data-stu-id="78630-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78630-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78630-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78630-132">DLL</span><span class="sxs-lookup"><span data-stu-id="78630-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78630-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78630-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78630-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78630-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78630-135">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="78630-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

