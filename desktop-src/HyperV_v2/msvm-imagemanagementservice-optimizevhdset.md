---
description: Оптимизирует файл набора виртуальных жестких дисков для использования меньшего места на диске.
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Метод Оптимизевхдсет класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897702"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="6b97a-103">Метод Оптимизевхдсет \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="6b97a-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="6b97a-104">Оптимизирует файл набора виртуальных жестких дисков для использования меньшего места на диске.</span><span class="sxs-lookup"><span data-stu-id="6b97a-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b97a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b97a-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6b97a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b97a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b97a-107">*Вхдсетпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b97a-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b97a-108">Полный путь, указывающий расположение файла набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="6b97a-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="6b97a-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b97a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b97a-110">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="6b97a-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b97a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b97a-111">Return value</span></span>

<span data-ttu-id="6b97a-112">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6b97a-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6b97a-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6b97a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6b97a-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6b97a-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6b97a-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6b97a-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6b97a-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6b97a-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6b97a-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="6b97a-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="6b97a-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="6b97a-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="6b97a-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="6b97a-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6b97a-126">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="6b97a-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6b97a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6b97a-127">Requirements</span></span>



| <span data-ttu-id="6b97a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6b97a-128">Requirement</span></span> | <span data-ttu-id="6b97a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6b97a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b97a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b97a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6b97a-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6b97a-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6b97a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b97a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6b97a-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6b97a-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6b97a-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b97a-134">Namespace</span></span><br/>                | <span data-ttu-id="6b97a-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6b97a-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6b97a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6b97a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b97a-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b97a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b97a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6b97a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b97a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b97a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b97a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b97a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b97a-141">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="6b97a-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




