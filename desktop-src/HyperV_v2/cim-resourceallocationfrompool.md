---
description: Представляет ассоциацию, в которой \_ экземпляр CIM ресаурцеаллокатионсеттингдата выделяется из пула ресурсов.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: Класс CIM_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999034"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="0ac70-103">\_Класс CIM ресаурцеаллокатионфромпул</span><span class="sxs-lookup"><span data-stu-id="0ac70-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="0ac70-104">Представляет ассоциацию, в которой экземпляр [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) выделяется из пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ac70-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ac70-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0ac70-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0ac70-106">Members</span></span>

<span data-ttu-id="0ac70-107">Класс **CIM \_ ресаурцеаллокатионфромпул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0ac70-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="0ac70-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ac70-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ac70-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ac70-109">Properties</span></span>

<span data-ttu-id="0ac70-110">Класс **CIM \_ ресаурцеаллокатионфромпул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0ac70-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ac70-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0ac70-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac70-112">Тип данных: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="0ac70-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="0ac70-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ac70-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ac70-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0ac70-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0ac70-115">Пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ac70-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="0ac70-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="0ac70-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac70-117">Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="0ac70-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="0ac70-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ac70-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ac70-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="0ac70-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0ac70-120">Данные о выделении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ac70-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ac70-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0ac70-121">Requirements</span></span>



| <span data-ttu-id="0ac70-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0ac70-122">Requirement</span></span> | <span data-ttu-id="0ac70-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac70-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac70-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ac70-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac70-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0ac70-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0ac70-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ac70-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac70-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ac70-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0ac70-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ac70-128">Namespace</span></span><br/>                | <span data-ttu-id="0ac70-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0ac70-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0ac70-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0ac70-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ac70-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ac70-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ac70-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0ac70-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ac70-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ac70-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ac70-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ac70-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac70-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="0ac70-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

