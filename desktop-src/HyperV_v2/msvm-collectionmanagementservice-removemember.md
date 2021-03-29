---
description: Удаляет указанный управляемый элемент в качестве члена данного \_ объекта КОЛЛЕКТИОНОФМСЕС CIM.
ms.assetid: ea945d24-bcff-476b-9adb-c6573cdbc0b5
title: Метод Ремовемембер класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 894230dcf5e9a537ca444815f8e941a8e6fcf09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912587"
---
# <a name="removemember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="f531a-103">Метод Ремовемембер \_ класса Коллектионманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f531a-103">RemoveMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="f531a-104">Удаляет указанный управляемый элемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="f531a-104">Removes the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f531a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f531a-105">Syntax</span></span>


```mof
uint32 RemoveMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f531a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f531a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f531a-107">*Элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f531a-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f531a-108">Удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="f531a-108">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="f531a-109">*Коллекция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f531a-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f531a-110">Коллекция, из которой удаляется элемент.</span><span class="sxs-lookup"><span data-stu-id="f531a-110">The collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="f531a-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f531a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f531a-112">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="f531a-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f531a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f531a-113">Return value</span></span>

<span data-ttu-id="f531a-114">Возвращает 0 в случае успеха или 4096, если задание запущено; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f531a-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f531a-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f531a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f531a-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f531a-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f531a-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f531a-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f531a-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f531a-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f531a-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f531a-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f531a-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f531a-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f531a-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f531a-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f531a-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="f531a-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f531a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f531a-129">Requirements</span></span>



| <span data-ttu-id="f531a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f531a-130">Requirement</span></span> | <span data-ttu-id="f531a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f531a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f531a-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f531a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f531a-133">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f531a-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f531a-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f531a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f531a-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f531a-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f531a-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f531a-136">Namespace</span></span><br/>                | <span data-ttu-id="f531a-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f531a-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f531a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f531a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f531a-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f531a-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f531a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f531a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f531a-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f531a-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f531a-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f531a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f531a-143">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="f531a-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




