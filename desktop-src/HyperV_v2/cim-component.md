---
description: Представляет универсальную связь между родительским управляемым элементом и дочерним управляемым элементом, в котором дочерний элемент представляет компонент или часть родительского элемента.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Класс CIM_Component (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683619"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="69847-103">Класс CIM_Component (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="69847-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="69847-104">Представляет универсальную связь между родительским управляемым элементом и дочерним управляемым элементом, в котором дочерний элемент представляет компонент или часть родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="69847-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="69847-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69847-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="69847-106">Члены</span><span class="sxs-lookup"><span data-stu-id="69847-106">Members</span></span>

<span data-ttu-id="69847-107">Класс **\_ компонента CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="69847-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="69847-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="69847-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69847-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="69847-109">Properties</span></span>

<span data-ttu-id="69847-110">Класс **\_ компонента CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="69847-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69847-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="69847-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69847-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="69847-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="69847-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="69847-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69847-114">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**агрегатная функция**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="69847-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="69847-115">Родительский элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="69847-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="69847-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="69847-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69847-117">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="69847-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="69847-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="69847-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69847-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="69847-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="69847-120">Дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="69847-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69847-121">Требования</span><span class="sxs-lookup"><span data-stu-id="69847-121">Requirements</span></span>



| <span data-ttu-id="69847-122">Требование</span><span class="sxs-lookup"><span data-stu-id="69847-122">Requirement</span></span> | <span data-ttu-id="69847-123">Значение</span><span class="sxs-lookup"><span data-stu-id="69847-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69847-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69847-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69847-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="69847-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="69847-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69847-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69847-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69847-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="69847-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="69847-128">Namespace</span></span><br/>                | <span data-ttu-id="69847-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="69847-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="69847-130">MOF</span><span class="sxs-lookup"><span data-stu-id="69847-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69847-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69847-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69847-132">DLL</span><span class="sxs-lookup"><span data-stu-id="69847-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69847-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69847-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

