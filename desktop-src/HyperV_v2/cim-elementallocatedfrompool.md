---
description: Представляет ассоциацию, в которой \_ объект CIM логикалелемент представляет ресурс, выделенный из \_ объекта ResourcePool CIM.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: Класс CIM_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897885"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="552ea-103">\_Класс CIM елементаллокатедфромпул</span><span class="sxs-lookup"><span data-stu-id="552ea-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="552ea-104">Представляет ассоциацию, в которой объект [**CIM \_ логикалелемент**](cim-logicalelement.md) представляет ресурс, выделенный из [**объекта \_ ResourcePool CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="552ea-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="552ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="552ea-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="552ea-106">Члены</span><span class="sxs-lookup"><span data-stu-id="552ea-106">Members</span></span>

<span data-ttu-id="552ea-107">Класс **CIM \_ елементаллокатедфромпул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="552ea-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="552ea-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="552ea-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="552ea-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="552ea-109">Properties</span></span>

<span data-ttu-id="552ea-110">Класс **CIM \_ елементаллокатедфромпул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="552ea-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="552ea-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="552ea-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552ea-112">Тип данных: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="552ea-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="552ea-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="552ea-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="552ea-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="552ea-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="552ea-115">Пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="552ea-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="552ea-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="552ea-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="552ea-117">Тип данных: **CIM \_ логикалелемент**</span><span class="sxs-lookup"><span data-stu-id="552ea-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="552ea-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="552ea-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="552ea-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="552ea-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="552ea-120">Выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="552ea-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="552ea-121">Требования</span><span class="sxs-lookup"><span data-stu-id="552ea-121">Requirements</span></span>



| <span data-ttu-id="552ea-122">Требование</span><span class="sxs-lookup"><span data-stu-id="552ea-122">Requirement</span></span> | <span data-ttu-id="552ea-123">Значение</span><span class="sxs-lookup"><span data-stu-id="552ea-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552ea-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="552ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="552ea-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="552ea-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="552ea-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="552ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="552ea-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="552ea-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="552ea-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="552ea-128">Namespace</span></span><br/>                | <span data-ttu-id="552ea-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="552ea-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="552ea-130">MOF</span><span class="sxs-lookup"><span data-stu-id="552ea-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="552ea-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="552ea-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="552ea-132">DLL</span><span class="sxs-lookup"><span data-stu-id="552ea-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552ea-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="552ea-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="552ea-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="552ea-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552ea-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="552ea-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

