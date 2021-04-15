---
description: Служба для создания, уничтожения и экспорта опорных точек.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Класс Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682935"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="9fedf-103">\_Класс мсвм коллектионреференцепоинтсервице</span><span class="sxs-lookup"><span data-stu-id="9fedf-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="9fedf-104">Служба для создания, уничтожения и экспорта опорных точек</span><span class="sxs-lookup"><span data-stu-id="9fedf-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="9fedf-105">коллекций виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="9fedf-105">of virtual system collections.</span></span>

<span data-ttu-id="9fedf-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9fedf-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fedf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fedf-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="9fedf-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9fedf-108">Members</span></span>

<span data-ttu-id="9fedf-109">Класс **мсвм \_ коллектионреференцепоинтсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9fedf-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="9fedf-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9fedf-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9fedf-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9fedf-111">Methods</span></span>

<span data-ttu-id="9fedf-112">Класс **мсвм \_ коллектионреференцепоинтсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9fedf-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="9fedf-113">Метод</span><span class="sxs-lookup"><span data-stu-id="9fedf-113">Method</span></span>                                                                                      | <span data-ttu-id="9fedf-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9fedf-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fedf-115">**креатереференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="9fedf-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="9fedf-116">Создает точку ссылки для коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="9fedf-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="9fedf-117">**дестройреференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="9fedf-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="9fedf-118">Уничтожает существующую коллекцию опорных точек.</span><span class="sxs-lookup"><span data-stu-id="9fedf-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="9fedf-119">Этот метод может в качестве побочного действия уничтожить другие опорные точки, зависящие от затронутой коллекции опорных точек.</span><span class="sxs-lookup"><span data-stu-id="9fedf-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="9fedf-120">**експортреференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="9fedf-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="9fedf-121">Экспортирует коллекцию опорных точек в файл.</span><span class="sxs-lookup"><span data-stu-id="9fedf-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="9fedf-122">Коллекция опорных точек, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.</span><span class="sxs-lookup"><span data-stu-id="9fedf-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="9fedf-123">**ремовеассоЦиатеддата**</span><span class="sxs-lookup"><span data-stu-id="9fedf-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="9fedf-124">Удаляет журнал данных, связанный с точкой ссылки.</span><span class="sxs-lookup"><span data-stu-id="9fedf-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="9fedf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9fedf-125">Requirements</span></span>



| <span data-ttu-id="9fedf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9fedf-126">Requirement</span></span> | <span data-ttu-id="9fedf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9fedf-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fedf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fedf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9fedf-129">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9fedf-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9fedf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fedf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9fedf-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9fedf-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9fedf-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9fedf-132">Namespace</span></span><br/>                | <span data-ttu-id="9fedf-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9fedf-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9fedf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9fedf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fedf-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fedf-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fedf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9fedf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fedf-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fedf-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9fedf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fedf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fedf-139">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="9fedf-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




