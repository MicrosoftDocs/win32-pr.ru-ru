---
description: Создает новый объект CIM \_ коллектионофмсес.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Метод Дефинеколлектион класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684276"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="562c5-103">Метод Дефинеколлектион \_ класса Коллектионманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="562c5-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="562c5-104">Создает новый объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="562c5-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="562c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="562c5-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="562c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="562c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="562c5-107">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="562c5-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562c5-108">Имя новой коллекции.</span><span class="sxs-lookup"><span data-stu-id="562c5-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="562c5-109">*Идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="562c5-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562c5-110">Идентификатор новой коллекции.</span><span class="sxs-lookup"><span data-stu-id="562c5-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="562c5-111">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="562c5-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562c5-112">Тип новой коллекции.</span><span class="sxs-lookup"><span data-stu-id="562c5-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="562c5-113">**Коллекция виртуальных систем** (0)</span><span class="sxs-lookup"><span data-stu-id="562c5-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="562c5-114">**Коллекция коллекций** (1)</span><span class="sxs-lookup"><span data-stu-id="562c5-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="562c5-115">*Дефинедколлектион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="562c5-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="562c5-116">Ссылка на объекты, определяющие коллекцию.</span><span class="sxs-lookup"><span data-stu-id="562c5-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="562c5-117">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="562c5-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="562c5-118">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="562c5-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="562c5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="562c5-119">Return value</span></span>

<span data-ttu-id="562c5-120">В случае успеха возвращает 0 или 4096 (задание запущено); в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="562c5-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="562c5-121">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="562c5-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="562c5-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-123">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="562c5-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-124">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="562c5-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-125">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="562c5-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-126">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="562c5-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-127">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="562c5-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-128">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="562c5-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-129">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="562c5-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-130">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="562c5-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-131">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="562c5-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-132">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="562c5-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-133">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="562c5-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="562c5-134">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="562c5-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="562c5-135">Требования</span><span class="sxs-lookup"><span data-stu-id="562c5-135">Requirements</span></span>



| <span data-ttu-id="562c5-136">Требование</span><span class="sxs-lookup"><span data-stu-id="562c5-136">Requirement</span></span> | <span data-ttu-id="562c5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="562c5-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="562c5-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="562c5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="562c5-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="562c5-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="562c5-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="562c5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="562c5-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="562c5-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="562c5-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="562c5-142">Namespace</span></span><br/>                | <span data-ttu-id="562c5-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="562c5-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="562c5-144">MOF</span><span class="sxs-lookup"><span data-stu-id="562c5-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="562c5-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="562c5-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="562c5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="562c5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="562c5-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="562c5-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="562c5-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="562c5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562c5-149">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="562c5-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




