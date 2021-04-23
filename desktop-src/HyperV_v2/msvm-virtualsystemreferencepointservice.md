---
description: Описывает службу опорной точки виртуальной системы.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Класс Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664803"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="6170b-103">\_Класс мсвм виртуалсистемреференцепоинтсервице</span><span class="sxs-lookup"><span data-stu-id="6170b-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="6170b-104">Описывает службу опорной точки виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="6170b-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="6170b-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6170b-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6170b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6170b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="6170b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6170b-107">Members</span></span>

<span data-ttu-id="6170b-108">Класс **мсвм \_ виртуалсистемреференцепоинтсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6170b-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="6170b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="6170b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6170b-110">Методы</span><span class="sxs-lookup"><span data-stu-id="6170b-110">Methods</span></span>

<span data-ttu-id="6170b-111">Класс **мсвм \_ виртуалсистемреференцепоинтсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6170b-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="6170b-112">Метод</span><span class="sxs-lookup"><span data-stu-id="6170b-112">Method</span></span>                                                                                                       | <span data-ttu-id="6170b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="6170b-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="6170b-114">**креатереференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="6170b-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="6170b-115">Создает опорную точку виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="6170b-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="6170b-116">**дестройреференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="6170b-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="6170b-117">Удаляет указанную точку ссылки.</span><span class="sxs-lookup"><span data-stu-id="6170b-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="6170b-118">**експортреференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="6170b-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="6170b-119">Экспортирует опорную точку виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="6170b-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="6170b-120">**импортреференцепоинтметадата**</span><span class="sxs-lookup"><span data-stu-id="6170b-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="6170b-121">Импортирует метаданные опорной точки виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="6170b-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="6170b-122">**ремовеассоЦиатеддата**</span><span class="sxs-lookup"><span data-stu-id="6170b-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="6170b-123">Удаляет журнал данных, связанный с точкой ссылки.</span><span class="sxs-lookup"><span data-stu-id="6170b-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6170b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6170b-124">Requirements</span></span>



| <span data-ttu-id="6170b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6170b-125">Requirement</span></span> | <span data-ttu-id="6170b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6170b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6170b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6170b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6170b-128">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6170b-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6170b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6170b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6170b-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6170b-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6170b-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6170b-131">Namespace</span></span><br/>                | <span data-ttu-id="6170b-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6170b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6170b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6170b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6170b-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6170b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6170b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6170b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6170b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6170b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6170b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6170b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6170b-138">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="6170b-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




