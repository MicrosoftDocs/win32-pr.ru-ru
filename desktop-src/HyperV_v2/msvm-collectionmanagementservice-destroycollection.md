---
description: Удаляет данный объект CIM \_ коллектионофмсес.
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Метод Дестройколлектион класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684628"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="ffc5d-103">Метод Дестройколлектион \_ класса Коллектионманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="ffc5d-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="ffc5d-104">Удаляет данный объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc5d-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc5d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffc5d-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ffc5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffc5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc5d-107">*Коллекция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffc5d-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc5d-108">Коллекция для уничтожения.</span><span class="sxs-lookup"><span data-stu-id="ffc5d-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="ffc5d-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ffc5d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc5d-110">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="ffc5d-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffc5d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffc5d-111">Return value</span></span>

<span data-ttu-id="ffc5d-112">Возвращает 0 в случае успеха или 4096, если задание запущено; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ffc5d-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ffc5d-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ffc5d-126">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="ffc5d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ffc5d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ffc5d-127">Requirements</span></span>



| <span data-ttu-id="ffc5d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ffc5d-128">Requirement</span></span> | <span data-ttu-id="ffc5d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ffc5d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc5d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffc5d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc5d-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ffc5d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ffc5d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffc5d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc5d-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ffc5d-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ffc5d-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffc5d-134">Namespace</span></span><br/>                | <span data-ttu-id="ffc5d-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ffc5d-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffc5d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ffc5d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffc5d-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffc5d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffc5d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc5d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffc5d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffc5d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffc5d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffc5d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc5d-141">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="ffc5d-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




