---
description: Устанавливает, что экземпляр CIM \_ ресаурцеаллокатионсеттингдата, представляющий выделение ресурсов, зависит от выделения другого ресурса.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Класс Msvm_ResourceDependentOnResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683682"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="fd188-103">\_Класс мсвм ресаурцедепендентонресаурце</span><span class="sxs-lookup"><span data-stu-id="fd188-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="fd188-104">Устанавливает, что экземпляр [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий выделение ресурсов, зависит от выделения другого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fd188-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="fd188-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fd188-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd188-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd188-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fd188-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fd188-107">Members</span></span>

<span data-ttu-id="fd188-108">Класс **мсвм \_ ресаурцедепендентонресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fd188-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="fd188-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd188-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd188-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd188-110">Properties</span></span>

<span data-ttu-id="fd188-111">Класс **мсвм \_ ресаурцедепендентонресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fd188-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd188-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="fd188-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd188-113">Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="fd188-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="fd188-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd188-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd188-115">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="fd188-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fd188-116">[**\_ Ресаурцеаллокатионсеттингдата CIM**](cim-resourceallocationsettingdata.md) , представляющий независимый ресурс в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="fd188-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="fd188-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="fd188-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd188-118">Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="fd188-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="fd188-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fd188-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd188-120">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="fd188-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fd188-121">[**\_ Ресаурцеаллокатионсеттингдата CIM**](cim-resourceallocationsettingdata.md) , представляющий ресурс, который зависит от предшествующей задачи.</span><span class="sxs-lookup"><span data-stu-id="fd188-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd188-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fd188-122">Requirements</span></span>



| <span data-ttu-id="fd188-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fd188-123">Requirement</span></span> | <span data-ttu-id="fd188-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fd188-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd188-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd188-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fd188-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fd188-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fd188-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd188-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fd188-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fd188-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fd188-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd188-129">Namespace</span></span><br/>                | <span data-ttu-id="fd188-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fd188-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fd188-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fd188-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd188-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd188-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd188-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fd188-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd188-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd188-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd188-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd188-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd188-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="fd188-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

