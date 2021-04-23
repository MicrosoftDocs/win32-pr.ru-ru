---
description: Обновляет имя элемента для указанного \_ объекта CIM коллектионофмсес.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Метод Ренамеколлектион класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912584"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="cf1be-103">Метод Ренамеколлектион \_ класса Коллектионманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="cf1be-103">RenameCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="cf1be-104">Обновляет имя элемента для указанного объекта [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1be-104">Updates the element name for the specified [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf1be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf1be-105">Syntax</span></span>


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cf1be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf1be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf1be-107">*Коллекция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf1be-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf1be-108">Коллекция для переименования.</span><span class="sxs-lookup"><span data-stu-id="cf1be-108">The collection to rename.</span></span>

</dd> <dt>

<span data-ttu-id="cf1be-109">*Новое_имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf1be-109">*NewName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf1be-110">Новое имя для использования.</span><span class="sxs-lookup"><span data-stu-id="cf1be-110">The new name to use.</span></span>

</dd> <dt>

<span data-ttu-id="cf1be-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf1be-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf1be-112">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="cf1be-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf1be-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf1be-113">Return value</span></span>

<span data-ttu-id="cf1be-114">Возвращает 0 в случае успеха или 4096, если задание запущено; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf1be-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="cf1be-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="cf1be-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="cf1be-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="cf1be-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="cf1be-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="cf1be-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="cf1be-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="cf1be-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="cf1be-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="cf1be-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="cf1be-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="cf1be-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="cf1be-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="cf1be-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="cf1be-128">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="cf1be-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cf1be-129">Требования</span><span class="sxs-lookup"><span data-stu-id="cf1be-129">Requirements</span></span>



| <span data-ttu-id="cf1be-130">Требование</span><span class="sxs-lookup"><span data-stu-id="cf1be-130">Requirement</span></span> | <span data-ttu-id="cf1be-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cf1be-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1be-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf1be-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cf1be-133">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cf1be-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cf1be-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf1be-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cf1be-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cf1be-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cf1be-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf1be-136">Namespace</span></span><br/>                | <span data-ttu-id="cf1be-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cf1be-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cf1be-138">MOF</span><span class="sxs-lookup"><span data-stu-id="cf1be-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf1be-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf1be-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf1be-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cf1be-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf1be-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf1be-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf1be-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf1be-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1be-143">**Мсвм \_ коллектионманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="cf1be-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




