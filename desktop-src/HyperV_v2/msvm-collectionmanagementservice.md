---
description: Управляет коллекциями на узле Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Класс Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819017"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="94b4d-103">\_Класс мсвм коллектионманажементсервице</span><span class="sxs-lookup"><span data-stu-id="94b4d-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="94b4d-104">Управляет коллекциями на узле Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="94b4d-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="94b4d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="94b4d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b4d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94b4d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="94b4d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="94b4d-107">Members</span></span>

<span data-ttu-id="94b4d-108">Класс **мсвм \_ коллектионманажементсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="94b4d-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="94b4d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="94b4d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94b4d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="94b4d-110">Methods</span></span>

<span data-ttu-id="94b4d-111">Класс **мсвм \_ коллектионманажементсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="94b4d-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="94b4d-112">Метод</span><span class="sxs-lookup"><span data-stu-id="94b4d-112">Method</span></span>                                                                          | <span data-ttu-id="94b4d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="94b4d-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94b4d-114">**аддмембер**</span><span class="sxs-lookup"><span data-stu-id="94b4d-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="94b4d-115">Добавляет указанный Манажеделемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="94b4d-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="94b4d-116">**дефинеколлектион**</span><span class="sxs-lookup"><span data-stu-id="94b4d-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="94b4d-117">Создает новый объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="94b4d-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="94b4d-118">**дестройколлектион**</span><span class="sxs-lookup"><span data-stu-id="94b4d-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="94b4d-119">Удаляет данный объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="94b4d-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="94b4d-120">**ремовемембер**</span><span class="sxs-lookup"><span data-stu-id="94b4d-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="94b4d-121">Удаляет указанный Манажеделемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="94b4d-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="94b4d-122">**ремовемембербид**</span><span class="sxs-lookup"><span data-stu-id="94b4d-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="94b4d-123">Удаляет указанный Манажеделемент в качестве члена [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="94b4d-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="94b4d-124">Это будет выполняться, даже если объект с таким идентификатором отсутствует.</span><span class="sxs-lookup"><span data-stu-id="94b4d-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="94b4d-125">**ренамеколлектион**</span><span class="sxs-lookup"><span data-stu-id="94b4d-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="94b4d-126">Обновляет ElementName заданного объекта [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="94b4d-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="94b4d-127">**StartService**</span><span class="sxs-lookup"><span data-stu-id="94b4d-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="94b4d-128">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="94b4d-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="94b4d-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="94b4d-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="94b4d-130">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="94b4d-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="94b4d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="94b4d-131">Requirements</span></span>



| <span data-ttu-id="94b4d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="94b4d-132">Requirement</span></span> | <span data-ttu-id="94b4d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="94b4d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94b4d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94b4d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="94b4d-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="94b4d-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="94b4d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94b4d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="94b4d-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="94b4d-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="94b4d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="94b4d-138">Namespace</span></span><br/>                | <span data-ttu-id="94b4d-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="94b4d-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="94b4d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="94b4d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94b4d-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94b4d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94b4d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="94b4d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b4d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94b4d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94b4d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94b4d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b4d-145">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="94b4d-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




