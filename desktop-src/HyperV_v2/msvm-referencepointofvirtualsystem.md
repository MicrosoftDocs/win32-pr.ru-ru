---
description: Связывает виртуалсистемреференцепоинт Мсвм \_ с соответствующими \_ объектами мсвм виртуалсистем.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Класс Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814217"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="9d02b-103">\_Класс мсвм референцепоинтофвиртуалсистем</span><span class="sxs-lookup"><span data-stu-id="9d02b-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="9d02b-104">Связывает [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) с соответствующими объектами [**мсвм \_ виртуалсистем**](msvm-virtualsystemresourcecomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="9d02b-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="9d02b-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9d02b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d02b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d02b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9d02b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9d02b-107">Members</span></span>

<span data-ttu-id="9d02b-108">Класс **мсвм \_ референцепоинтофвиртуалсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d02b-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="9d02b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d02b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d02b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d02b-110">Properties</span></span>

<span data-ttu-id="9d02b-111">Класс **мсвм \_ референцепоинтофвиртуалсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9d02b-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d02b-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="9d02b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d02b-113">Тип данных: **мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="9d02b-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9d02b-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d02b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d02b-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="9d02b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9d02b-116">Объект [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющий независимый объект в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="9d02b-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="9d02b-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="9d02b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d02b-118">Тип данных: **мсвм \_ виртуалсистемреференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="9d02b-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="9d02b-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d02b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d02b-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="9d02b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9d02b-121">[**\_ Виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , представляющий объект, который зависит от **предшествующей задачи**.</span><span class="sxs-lookup"><span data-stu-id="9d02b-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d02b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9d02b-122">Requirements</span></span>



| <span data-ttu-id="9d02b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9d02b-123">Requirement</span></span> | <span data-ttu-id="9d02b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9d02b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d02b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d02b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d02b-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9d02b-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9d02b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d02b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d02b-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d02b-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9d02b-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d02b-129">Namespace</span></span><br/>                | <span data-ttu-id="9d02b-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9d02b-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9d02b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9d02b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d02b-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d02b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d02b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9d02b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d02b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d02b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d02b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d02b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d02b-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="9d02b-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

