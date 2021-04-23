---
description: Представляет службу, которая управляет виртуальными системами.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: Класс CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662995"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="9ad93-103">\_Класс CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="9ad93-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="9ad93-104">Представляет службу, которая управляет виртуальными системами.</span><span class="sxs-lookup"><span data-stu-id="9ad93-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ad93-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="9ad93-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9ad93-106">Members</span></span>

<span data-ttu-id="9ad93-107">Класс **CIM \_ виртуалсистемманажементсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ad93-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="9ad93-108">Методы</span><span class="sxs-lookup"><span data-stu-id="9ad93-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9ad93-109">Методы</span><span class="sxs-lookup"><span data-stu-id="9ad93-109">Methods</span></span>

<span data-ttu-id="9ad93-110">Класс **CIM \_ виртуалсистемманажементсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9ad93-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="9ad93-111">Метод</span><span class="sxs-lookup"><span data-stu-id="9ad93-111">Method</span></span>                                                                                      | <span data-ttu-id="9ad93-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9ad93-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad93-113">**аддресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="9ad93-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="9ad93-114">Добавляет ресурсы в конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="9ad93-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="9ad93-115">**дефинесистем**</span><span class="sxs-lookup"><span data-stu-id="9ad93-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="9ad93-116">Определяет виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="9ad93-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="9ad93-117">**дестройсистем**</span><span class="sxs-lookup"><span data-stu-id="9ad93-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="9ad93-118">Удаляет виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="9ad93-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="9ad93-119">**модифиресаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="9ad93-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="9ad93-120">Изменяет параметры виртуального ресурса для конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="9ad93-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="9ad93-121">**модифисистемсеттингс**</span><span class="sxs-lookup"><span data-stu-id="9ad93-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="9ad93-122">Изменяет параметры виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="9ad93-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="9ad93-123">**ремовересаурцесеттингс**</span><span class="sxs-lookup"><span data-stu-id="9ad93-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="9ad93-124">Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="9ad93-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="9ad93-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9ad93-125">Requirements</span></span>



| <span data-ttu-id="9ad93-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9ad93-126">Requirement</span></span> | <span data-ttu-id="9ad93-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9ad93-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad93-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ad93-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad93-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9ad93-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9ad93-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ad93-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad93-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ad93-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9ad93-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ad93-132">Namespace</span></span><br/>                | <span data-ttu-id="9ad93-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9ad93-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9ad93-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9ad93-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ad93-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ad93-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ad93-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9ad93-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ad93-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9ad93-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9ad93-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ad93-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad93-139">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="9ad93-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




