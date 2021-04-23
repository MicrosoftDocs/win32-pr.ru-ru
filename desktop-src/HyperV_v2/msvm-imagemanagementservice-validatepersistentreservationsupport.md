---
description: Проверяет, может ли файловая система поддерживать виртуальный жесткий диск с включенным постоянным резервированием.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Метод Валидатеперсистентресерватионсуппорт класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991225"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="eaf7a-103">Метод Валидатеперсистентресерватионсуппорт \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="eaf7a-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="eaf7a-104">Проверяет, может ли файловая система поддерживать виртуальный жесткий диск с включенным постоянным резервированием.</span><span class="sxs-lookup"><span data-stu-id="eaf7a-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf7a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eaf7a-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="eaf7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaf7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf7a-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eaf7a-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf7a-108">Полный путь, указывающий расположение файла образа диска или каталог, в котором может быть размещен файл образа диска.</span><span class="sxs-lookup"><span data-stu-id="eaf7a-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="eaf7a-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eaf7a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf7a-110">Ссылка на задание (может иметь значение null, если задача завершена успешно).</span><span class="sxs-lookup"><span data-stu-id="eaf7a-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf7a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eaf7a-111">Return value</span></span>

<span data-ttu-id="eaf7a-112">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="eaf7a-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="eaf7a-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="eaf7a-126">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="eaf7a-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eaf7a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="eaf7a-127">Requirements</span></span>



| <span data-ttu-id="eaf7a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="eaf7a-128">Requirement</span></span> | <span data-ttu-id="eaf7a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="eaf7a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf7a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eaf7a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf7a-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="eaf7a-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="eaf7a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eaf7a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf7a-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="eaf7a-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="eaf7a-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eaf7a-134">Namespace</span></span><br/>                | <span data-ttu-id="eaf7a-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="eaf7a-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eaf7a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="eaf7a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaf7a-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaf7a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaf7a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf7a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaf7a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eaf7a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eaf7a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eaf7a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf7a-141">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="eaf7a-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




