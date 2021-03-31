---
description: Представляет универсальную ассоциацию, используемую для установки частей связи между управляемыми элементами.
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: Класс CIM_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910400"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="51f55-103">\_Класс CIM конкретекомпонент</span><span class="sxs-lookup"><span data-stu-id="51f55-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="51f55-104">Представляет универсальную ассоциацию, используемую для установки частей связи между управляемыми элементами.</span><span class="sxs-lookup"><span data-stu-id="51f55-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51f55-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="51f55-106">Члены</span><span class="sxs-lookup"><span data-stu-id="51f55-106">Members</span></span>

<span data-ttu-id="51f55-107">Класс **CIM \_ конкретекомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="51f55-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="51f55-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="51f55-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51f55-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="51f55-109">Properties</span></span>

<span data-ttu-id="51f55-110">Класс **CIM \_ конкретекомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="51f55-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51f55-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="51f55-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51f55-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="51f55-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="51f55-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51f55-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51f55-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="51f55-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="51f55-115">Родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="51f55-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="51f55-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="51f55-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51f55-117">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="51f55-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="51f55-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51f55-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51f55-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="51f55-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="51f55-120">Дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="51f55-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51f55-121">Требования</span><span class="sxs-lookup"><span data-stu-id="51f55-121">Requirements</span></span>



| <span data-ttu-id="51f55-122">Требование</span><span class="sxs-lookup"><span data-stu-id="51f55-122">Requirement</span></span> | <span data-ttu-id="51f55-123">Значение</span><span class="sxs-lookup"><span data-stu-id="51f55-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f55-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51f55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="51f55-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="51f55-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="51f55-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51f55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="51f55-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51f55-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="51f55-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51f55-128">Namespace</span></span><br/>                | <span data-ttu-id="51f55-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="51f55-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="51f55-130">MOF</span><span class="sxs-lookup"><span data-stu-id="51f55-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51f55-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51f55-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51f55-132">DLL</span><span class="sxs-lookup"><span data-stu-id="51f55-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51f55-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51f55-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51f55-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51f55-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f55-135">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="51f55-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

