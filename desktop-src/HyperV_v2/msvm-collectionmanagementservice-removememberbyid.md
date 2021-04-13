---
description: Удаляет указанный управляемый элемент в качестве члена \_ КОЛЛЕКТИОНОФМСЕС CIM с заданным идентификатором. Это будет выполняться, даже если объект с таким идентификатором отсутствует.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Метод Ремовемембербид класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272963"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="7424a-104">Метод Ремовемембербид \_ класса Коллектионманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="7424a-104">RemoveMemberById method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="7424a-105">Удаляет указанный управляемый элемент в качестве члена [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="7424a-105">Removes the specified managed element as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="7424a-106">Это будет выполняться, даже если объект с таким идентификатором отсутствует.</span><span class="sxs-lookup"><span data-stu-id="7424a-106">This will succeed even if the object with that identifier is not present.</span></span>

## <a name="syntax"></a><span data-ttu-id="7424a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7424a-107">Syntax</span></span>


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7424a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7424a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7424a-109">*Элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7424a-109">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7424a-110">Удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="7424a-110">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="7424a-111">*CollectionId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7424a-111">*CollectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7424a-112">Идентификатор коллекции, из которой удаляется элемент.</span><span class="sxs-lookup"><span data-stu-id="7424a-112">The collection ID of the collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="7424a-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7424a-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7424a-114">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="7424a-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7424a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7424a-115">Return value</span></span>

<span data-ttu-id="7424a-116">Возвращает 0 в случае успеха или 4096, если задание запущено; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7424a-116">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7424a-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="7424a-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="7424a-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="7424a-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="7424a-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="7424a-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="7424a-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="7424a-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="7424a-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="7424a-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="7424a-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="7424a-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="7424a-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="7424a-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7424a-130">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="7424a-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7424a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7424a-131">Requirements</span></span>



| <span data-ttu-id="7424a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7424a-132">Requirement</span></span> | <span data-ttu-id="7424a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7424a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7424a-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7424a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7424a-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7424a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7424a-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7424a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7424a-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7424a-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7424a-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7424a-138">Namespace</span></span><br/>                | <span data-ttu-id="7424a-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7424a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7424a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7424a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7424a-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7424a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7424a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7424a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7424a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7424a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7424a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7424a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7424a-145">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="7424a-145">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




