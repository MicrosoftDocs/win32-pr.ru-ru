---
description: Представляет службу, которая может создавать, применять и удалять моментальные снимки виртуальных систем.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: Класс CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913900"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="5f85d-103">\_Класс CIM виртуалсистемснапшотсервице</span><span class="sxs-lookup"><span data-stu-id="5f85d-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="5f85d-104">Представляет службу, которая может создавать, применять и удалять моментальные снимки виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="5f85d-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f85d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f85d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="5f85d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5f85d-106">Members</span></span>

<span data-ttu-id="5f85d-107">Класс **CIM \_ виртуалсистемснапшотсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5f85d-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="5f85d-108">Методы</span><span class="sxs-lookup"><span data-stu-id="5f85d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5f85d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="5f85d-109">Methods</span></span>

<span data-ttu-id="5f85d-110">Класс **CIM \_ виртуалсистемснапшотсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5f85d-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="5f85d-111">Метод</span><span class="sxs-lookup"><span data-stu-id="5f85d-111">Method</span></span>                                                                      | <span data-ttu-id="5f85d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5f85d-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f85d-113">**апплиснапшот**</span><span class="sxs-lookup"><span data-stu-id="5f85d-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="5f85d-114">Применяет моментальный снимок виртуальной системы к виртуальной системе в исходной виртуальной системе.</span><span class="sxs-lookup"><span data-stu-id="5f85d-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="5f85d-115">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="5f85d-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="5f85d-116">Создает моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="5f85d-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="5f85d-117">**дестройснапшот**</span><span class="sxs-lookup"><span data-stu-id="5f85d-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="5f85d-118">Удаляет моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="5f85d-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="5f85d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5f85d-119">Requirements</span></span>



| <span data-ttu-id="5f85d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5f85d-120">Requirement</span></span> | <span data-ttu-id="5f85d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5f85d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f85d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f85d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f85d-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5f85d-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5f85d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f85d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f85d-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f85d-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5f85d-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5f85d-126">Namespace</span></span><br/>                | <span data-ttu-id="5f85d-127">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5f85d-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5f85d-128">MOF</span><span class="sxs-lookup"><span data-stu-id="5f85d-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f85d-129"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f85d-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f85d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5f85d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f85d-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f85d-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5f85d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f85d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f85d-133">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="5f85d-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




