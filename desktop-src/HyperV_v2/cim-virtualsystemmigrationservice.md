---
description: Представляет службу, управляющую переносом виртуальных систем между системами узлов. Этот класс также проверяет, вероятна ли успешная миграция.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Класс CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909191"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="0f102-104">\_Класс CIM виртуалсистеммигратионсервице</span><span class="sxs-lookup"><span data-stu-id="0f102-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="0f102-105">Представляет службу, управляющую переносом виртуальных систем между системами узлов.</span><span class="sxs-lookup"><span data-stu-id="0f102-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="0f102-106">Этот класс также проверяет, вероятна ли успешная миграция.</span><span class="sxs-lookup"><span data-stu-id="0f102-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f102-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f102-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="0f102-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0f102-108">Members</span></span>

<span data-ttu-id="0f102-109">Класс **CIM \_ виртуалсистеммигратионсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f102-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="0f102-110">Методы</span><span class="sxs-lookup"><span data-stu-id="0f102-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0f102-111">Методы</span><span class="sxs-lookup"><span data-stu-id="0f102-111">Methods</span></span>

<span data-ttu-id="0f102-112">Класс **CIM \_ виртуалсистеммигратионсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0f102-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="0f102-113">Метод</span><span class="sxs-lookup"><span data-stu-id="0f102-113">Method</span></span>                                                                                                                     | <span data-ttu-id="0f102-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0f102-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f102-115">**чекквиртуалсистемисмигратаблетохост**</span><span class="sxs-lookup"><span data-stu-id="0f102-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="0f102-116">Проверяет, вероятна ли успешная миграция виртуальной системы на узел.</span><span class="sxs-lookup"><span data-stu-id="0f102-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="0f102-117">**чекквиртуалсистемисмигратаблетосистем**</span><span class="sxs-lookup"><span data-stu-id="0f102-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="0f102-118">Проверяет, вероятна ли успешная миграция виртуальной системы в систему.</span><span class="sxs-lookup"><span data-stu-id="0f102-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="0f102-119">**мигратевиртуалсистемтохост**</span><span class="sxs-lookup"><span data-stu-id="0f102-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="0f102-120">Переносит виртуальную систему на целевой узел.</span><span class="sxs-lookup"><span data-stu-id="0f102-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="0f102-121">**мигратевиртуалсистемтосистем**</span><span class="sxs-lookup"><span data-stu-id="0f102-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="0f102-122">Переносит виртуальную систему в целевую систему.</span><span class="sxs-lookup"><span data-stu-id="0f102-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="0f102-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0f102-123">Requirements</span></span>



| <span data-ttu-id="0f102-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0f102-124">Requirement</span></span> | <span data-ttu-id="0f102-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0f102-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f102-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f102-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f102-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f102-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0f102-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f102-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f102-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f102-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0f102-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f102-130">Namespace</span></span><br/>                | <span data-ttu-id="0f102-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0f102-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f102-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0f102-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f102-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f102-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f102-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0f102-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f102-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f102-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f102-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f102-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f102-137">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="0f102-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




