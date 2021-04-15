---
description: Представляет универсальную ассоциацию, в которой управляемый элемент зависит от другого. CIM \_ конкретедепенденци подклассировать \_ зависимость CIM для предоставления конкретной версии класса \_ зависимости CIM.
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: Класс CIM_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683986"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="a562b-104">\_Класс CIM конкретедепенденци</span><span class="sxs-lookup"><span data-stu-id="a562b-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="a562b-105">Представляет универсальную ассоциацию, в которой управляемый элемент зависит от другого.</span><span class="sxs-lookup"><span data-stu-id="a562b-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="a562b-106">**Модель CIM \_ Конкретедепенденци** подклассировать [**\_ зависимость CIM**](cim-dependency.md) для предоставления конкретной версии класса **\_ зависимости CIM**.</span><span class="sxs-lookup"><span data-stu-id="a562b-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a562b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a562b-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a562b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a562b-108">Members</span></span>

<span data-ttu-id="a562b-109">Класс **CIM \_ конкретедепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a562b-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="a562b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a562b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a562b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a562b-111">Properties</span></span>

<span data-ttu-id="a562b-112">Класс **CIM \_ конкретедепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a562b-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a562b-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="a562b-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a562b-114">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="a562b-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a562b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a562b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a562b-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a562b-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a562b-117">Независимый объект в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="a562b-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a562b-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="a562b-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a562b-119">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="a562b-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a562b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a562b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a562b-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="a562b-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a562b-122">Зависимый объект в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="a562b-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a562b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a562b-123">Requirements</span></span>



| <span data-ttu-id="a562b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a562b-124">Requirement</span></span> | <span data-ttu-id="a562b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a562b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a562b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a562b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a562b-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a562b-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a562b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a562b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a562b-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a562b-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a562b-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a562b-130">Namespace</span></span><br/>                | <span data-ttu-id="a562b-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a562b-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a562b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a562b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a562b-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a562b-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a562b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a562b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a562b-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a562b-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a562b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a562b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a562b-137">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="a562b-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

