---
description: Добавляет указанный управляемый элемент в качестве члена данного \_ объекта КОЛЛЕКТИОНОФМСЕС CIM.
ms.assetid: 6f23eecc-b445-4495-ae96-76b89652a1cb
title: Метод Аддмембер класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.AddMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6b885701086262fda48c5d50abd750eca6866c72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819024"
---
# <a name="addmember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="ff0c1-103">Метод Аддмембер \_ класса Коллектионманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ff0c1-103">AddMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="ff0c1-104">Добавляет указанный управляемый элемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0c1-104">Adds the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff0c1-105">Syntax</span></span>


```mof
uint32 AddMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ff0c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff0c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0c1-107">*Элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff0c1-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0c1-108">Элемент, добавляемый в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="ff0c1-108">The member to add to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c1-109">*Коллекция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff0c1-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0c1-110">Коллекция, в которую добавляется элемент.</span><span class="sxs-lookup"><span data-stu-id="ff0c1-110">The collection to add the member to.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c1-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff0c1-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0c1-112">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="ff0c1-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0c1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff0c1-113">Return value</span></span>

<span data-ttu-id="ff0c1-114">Возвращает 0 в случае успеха или 4096, если задание запущено; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ff0c1-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ff0c1-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ff0c1-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="ff0c1-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ff0c1-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ff0c1-129">Requirements</span></span>



| <span data-ttu-id="ff0c1-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ff0c1-130">Requirement</span></span> | <span data-ttu-id="ff0c1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ff0c1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0c1-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff0c1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0c1-133">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ff0c1-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ff0c1-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff0c1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0c1-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ff0c1-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ff0c1-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ff0c1-136">Namespace</span></span><br/>                | <span data-ttu-id="ff0c1-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ff0c1-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ff0c1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ff0c1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff0c1-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff0c1-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff0c1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ff0c1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff0c1-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff0c1-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff0c1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff0c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0c1-143">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="ff0c1-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




