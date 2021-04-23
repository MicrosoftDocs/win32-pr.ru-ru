---
description: Представляет ассоциацию, в которой управляемый элемент размещается другим.
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: Класс CIM_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682418"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="1e503-103">\_Класс CIM хостеддепенденци</span><span class="sxs-lookup"><span data-stu-id="1e503-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="1e503-104">Представляет ассоциацию, в которой управляемый элемент размещается другим.</span><span class="sxs-lookup"><span data-stu-id="1e503-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e503-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e503-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1e503-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1e503-106">Members</span></span>

<span data-ttu-id="1e503-107">Класс **CIM \_ хостеддепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1e503-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="1e503-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e503-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e503-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e503-109">Properties</span></span>

<span data-ttu-id="1e503-110">Класс **CIM \_ хостеддепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1e503-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e503-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="1e503-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e503-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="1e503-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1e503-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e503-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e503-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1e503-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1e503-115">Элемент управляемого узла.</span><span class="sxs-lookup"><span data-stu-id="1e503-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="1e503-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="1e503-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e503-117">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="1e503-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1e503-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e503-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e503-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="1e503-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1e503-120">Размещенный управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="1e503-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e503-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1e503-121">Requirements</span></span>



| <span data-ttu-id="1e503-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1e503-122">Requirement</span></span> | <span data-ttu-id="1e503-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1e503-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e503-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e503-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e503-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e503-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1e503-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e503-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e503-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e503-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1e503-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1e503-128">Namespace</span></span><br/>                | <span data-ttu-id="1e503-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1e503-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1e503-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1e503-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e503-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e503-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e503-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1e503-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e503-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e503-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e503-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e503-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e503-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="1e503-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

