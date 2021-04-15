---
description: Служба для создания, уничтожения и экспорта снимков коллекции виртуальных систем.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Класс Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662743"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="d55df-103">\_Класс мсвм коллектионснапшотсервице</span><span class="sxs-lookup"><span data-stu-id="d55df-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="d55df-104">Служба для создания, уничтожения и экспорта снимков коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="d55df-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="d55df-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d55df-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55df-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d55df-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="d55df-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d55df-107">Members</span></span>

<span data-ttu-id="d55df-108">Класс **мсвм \_ коллектионснапшотсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d55df-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="d55df-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d55df-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d55df-110">Методы</span><span class="sxs-lookup"><span data-stu-id="d55df-110">Methods</span></span>

<span data-ttu-id="d55df-111">Класс **мсвм \_ коллектионснапшотсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d55df-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="d55df-112">Метод</span><span class="sxs-lookup"><span data-stu-id="d55df-112">Method</span></span>                                                                                    | <span data-ttu-id="d55df-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d55df-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d55df-114">**апплиснапшот**</span><span class="sxs-lookup"><span data-stu-id="d55df-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="d55df-115">Применяет коллекцию моментальных снимков к коллекции виртуальных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="d55df-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="d55df-116">**конверттореференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="d55df-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="d55df-117">Преобразование существующего моментального снимка коллекции в коллекцию опорных точек.</span><span class="sxs-lookup"><span data-stu-id="d55df-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="d55df-118">Коллекция моментальных снимков удаляется как побочный результат.</span><span class="sxs-lookup"><span data-stu-id="d55df-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="d55df-119">В контрольные точки можно преобразовать только моментальные снимки восстановления.</span><span class="sxs-lookup"><span data-stu-id="d55df-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="d55df-120">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="d55df-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="d55df-121">Создает моментальный снимок коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="d55df-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="d55df-122">**дестройснапшот**</span><span class="sxs-lookup"><span data-stu-id="d55df-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="d55df-123">Уничтожает существующий моментальный снимок коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="d55df-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="d55df-124">Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d55df-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="d55df-125">**експортснапшот**</span><span class="sxs-lookup"><span data-stu-id="d55df-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="d55df-126">Экспортирует коллекцию моментальных снимков для систем виртуальных компьютеров в файл.</span><span class="sxs-lookup"><span data-stu-id="d55df-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="d55df-127">Коллекция моментальных снимков, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.</span><span class="sxs-lookup"><span data-stu-id="d55df-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d55df-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d55df-128">Requirements</span></span>



| <span data-ttu-id="d55df-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d55df-129">Requirement</span></span> | <span data-ttu-id="d55df-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d55df-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d55df-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d55df-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d55df-132">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d55df-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d55df-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d55df-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d55df-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d55df-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d55df-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d55df-135">Namespace</span></span><br/>                | <span data-ttu-id="d55df-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d55df-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d55df-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d55df-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d55df-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d55df-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d55df-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d55df-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d55df-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d55df-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d55df-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d55df-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55df-142">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="d55df-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




